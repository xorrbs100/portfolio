---
layout: post
title:  "Java"
date:   2020-10-21
excerpt: "자바 GUI를 활용한 프로그램 구현"
project: true
tag:
- java 
comments: true
---

## 풀코드 링크
* http://

![Main](https://user-images.githubusercontent.com/69500105/111898422-552ace80-8a69-11eb-8828-fe28d1b56a11.png)
<center>My fisrt project in Java</center>

## Used Skills
* Java
* JavaGUI
* That's all.

## 제작동기
자바 문법의 기초를 복습하며 
취업 전까지 자바에 대한 감각 유지

개념을 프로젝트에 적용하며 경험 축적

부족하다고 느낀 스레드를 중점적으로 활용

## 설계구조
Jframe 으로 구성된 메인 화면에 
JToolBar와 JComboBox를 활용하여
5가지의 프로그램을 사용할 수 있도록 구현
(두더지 잡기, 꽃, 경마, 사격 게임, 타이머)

![g2](https://user-images.githubusercontent.com/69500105/111898390-1268f680-8a69-11eb-9a70-ac5d3040b4fc.png)
<center>두더지잡기</center>

![g3](https://user-images.githubusercontent.com/69500105/111898436-6ecc1600-8a69-11eb-9697-6b2be8e7584a.png)

<center>사격게임</center>

![g4](https://user-images.githubusercontent.com/69500105/111898441-6ffd4300-8a69-11eb-9284-360254f94b7b.png)
<center>타이머</center>

![g1](https://user-images.githubusercontent.com/69500105/111898442-712e7000-8a69-11eb-8b88-2f9c0306c186.png)
<center>경마</center>

---

## 애로사항과 해결방법

* 스레드 시작 시 많은 양의 메모리가 잡혀 버벅거리는 현상이 생김 
*  while(n<50) {
		if(flag==true) {	
		rt= new RainThread(jp);
		try{
			Thread.sleep(300);
		}catch(InterruptedException e) {
			e.printStackTrace();
		}
		n++;
		}
* run() 메소드에 생성되는 스레드 개수를 50개로 제한

## 보안점
* 스레드 종료, 재시작시 생기는 문제에 대한 공부
* 자바의 기본 문법에 대한 재공부

## 느낀점
* 기본에 충실하자.




