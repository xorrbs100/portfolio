---
layout: post
title:  "SpringBoard"
date:   2021-03-20
excerpt: "Spring을 활용한 게시판CRUD+회원가입"
project: true
tag:
- java 
- jsp
- board
- join
- login
- MVC2
- Spring
- mybatis
- jquery
- script
- OracleDB
- CRUD
- REST
comments: false
---

## 풀코드 GitHub 링크
<https://github.com/xorrbs100/SpringBoard>

![springboard](https://user-images.githubusercontent.com/69500105/111940648-9d51fb80-8b12-11eb-8705-3544c1319250.png)

<center>보드리스트</center>  


## Used Skills
* Java
* JSP
* Spring
* MyBatis
* Script,Jquery
* Ajax
* OracleDB
* Apache-Tomcat 9.0

## 제작동기
* 학원에서 배우지 못한 프레임워크에 대한 필요성을 느낌
* 스프링 프레임워크 사용경험 축적
* MyBatis 사용경험 축적
* Script,Jqeury에 익숙해지기 위함
* api 사용법 공부
* 웹개발에 필요한 기술들을 익히기 위함

## 제작기간
* 2021-03-08 ~ 2021-03-15


## 구현 기능
* 로그인 - 로그인 시 아이디와 비밀번호 확인을 각각하여 어떤값이 틀렸는지를 확인가능
* 회원가입 - 아이디 중복체크 기능, 필수요소 미입력시 가입불가, 입력 패턴 정규식 함수로 지정, 실시간 비밀번호 일치 불일치 확인
* 게시판 리스트 - 카테고리 체크박스 조회, 총 글의 갯수, 페이징, 로그인 여부 확인 후 글쓰기 제어
* 게시판 뷰 - 로그인 , 비로그인 구분 후 업데이트, 삭제 제어
* 글 작성 , 게시글 업데이트 - 작성자ID를 출력, 수정자 ID를 출력
* 각 체크박스, 리스트는 따로 저장된 DB에 있는 값을 가져옴


## 패키지 구조
![springpac](https://user-images.githubusercontent.com/69500105/111941751-13576200-8b15-11eb-93e8-8565e4a41b42.png)

 
## 실행화면
 ![springboardLogin](https://user-images.githubusercontent.com/69500105/111940649-9dea9200-8b12-11eb-87ab-d1c6f3277556.png)
 <center>로그인후 보드리스트</center>  


![springjoin](https://user-images.githubusercontent.com/69500105/111940650-9e832880-8b12-11eb-8204-89dee48531f7.png)
<center>회원가입</center>  


![spriongcate](https://user-images.githubusercontent.com/69500105/111940653-9f1bbf00-8b12-11eb-8042-ee1083c48505.png)
<center>카테고리별 리스트 출력</center>  


![testview](https://user-images.githubusercontent.com/69500105/111940654-9f1bbf00-8b12-11eb-9ae5-064056dae769.png)
<center>비로그인시 게시글 출력</center>  



![logview](https://user-images.githubusercontent.com/69500105/111940660-a04cec00-8b12-11eb-8df1-e9db42c23935.png)
<center>로그인시 게시글 출력</center>  



![loginwrite](https://user-images.githubusercontent.com/69500105/111940659-9fb45580-8b12-11eb-8406-767d78681419.png)
<center>글작성</center>  



![update](https://user-images.githubusercontent.com/69500105/111940655-9f1bbf00-8b12-11eb-862d-39e8c16d3bb4.png)
<center>게시글 업데이트</center>  



![del](https://user-images.githubusercontent.com/69500105/111940656-9fb45580-8b12-11eb-856c-f9b4ae26dc60.png)
<center>게시글 삭제</center>  



---

## 애로사항과 문제점
* 처음 만들어보는 스프링 프로젝트였기 때문에 거의 모든것이 애로사항이었다.
* jsp설정을 euc-kr 로하여 DB에 한글 데이터를 입력할 때 한글 깨짐 현상이 발생
* 설정부분의 에러에서 시간이 많이 소모되었다.
* 여러 기술들을 사용해보기 위한 시행착오가 많았다


## 보안점
* 스프링 책과 친해지기
* serialize-직렬화 를 하니 한글이 제대로 들어갔다!
 
```
        $j("#submit").on("click",function(){
			if($j("#boardTitle").val()==""){
				alert("제목을 입력해주세요");
			}else{
			var $frm = $j('.boardWrite :input');
			var param = $frm.serialize();
			
```

* 스프링 부트에 대해 찾아보기


## 느낀점
* 역시나 객체지향 !!
* 프레임 워크가 좋긴좋다.
* 모르는걸 배우는건 항상 재밌다!
* 익숙해지자

## 추가예정
* 네이버 api 로그인 연동

