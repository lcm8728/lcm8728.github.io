---
layout: post
title: "Character counter"
date: 2018-09-08
author: lcm
categories: project
---
## 개발환경
- framework : Qt.5.11.1
- language : C++
- OS : Windows 10 64bit  

## 구상
자기소개서, 지원서 등의 서류를 작성할 때, 글자 수를 맞추는 것은 중요한 작업이다. 서류를 작성하는 사람들은 대게 다음과 같은 단계를 거쳐 글자 수를 맞추게 된다.  
- 텍스트 선택 -> 복사 -> 윈도우 활성화 -> 붙여넣기

이 프로그램은 위와 같은 과정을 줄이고자 만들여졌다. 이 프로그램으로 글자 수를 확인하는 단계는 다음과 같다.
- 텍스트 선택 -> 단축키 입력

## 구현
우선 프로그램의 창을 계속해서 불러와야 하는 과정을 없애기 위해, 윈도우를 항상 위에 있도록 하였다. 그리고 마찬가지의 이유로, 윈도우가 활성화 되어 있지 않을 때도 작동하게 하기 위하여 키보드 hooking을 가능하도록 하였다.  
위와 같은 매커니즘으로 다른 어플리케이션에서 단축키인 Ctrl + C + C가 입력되면 글자 수를 출력하게 된다. Ctrl + C 과정에서 클립보드에 글을 복사하고, 다시 한 번 C가 입력되는 순간 클립보드의 글자 수를 불러와 글자 수를 계산한다. 단축키는 어떤 에디터를 사용하더라도 문제가 없도록 설정하였다.  
  
## 실행화면
![text](/assets/character_counter_example1.png)  
  
  [https://github.com/lcm8728/character_counter](https://github.com/lcm8728/character_counter)
