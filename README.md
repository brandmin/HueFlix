# ⭐️Portfolio - HueFlix

 <!-- contents -->
<details open="open">
  <summary>Contents</summary>
  <ol>
    <li>
      <a href="#개요">개요</a>
    </li>
    <li>
      <a href="#내용">내용</a>
    </li>
    <li><a href="#구현기능">구현기능</a>
    
    </li>
  </ol>
</details>

-----------
# 📝개요
* 프로젝트 명: HueFlix

* 일정: 2023년 12월 6일 ~ 

* 개발 목적: 영화를 좋아하는 사용자들에게 다양한 정보를 제공하기 위한 웹 사이트 제작 

* 개발 환경
  - Server: Apache-tomcat-9.0.0
  - Java EE: Eclipse (version 2023-06)
  - Database: Oracle SQL developer
  - Language: Java, Jsp, HTML, CSS, JavaScript, SQL, Spring Legacy, mybatis
  - Framework: Spring Tool suite 3.9.1
----------
  # 📝내용
  
* 팀원 역할
  - 공통:  웹사이트 UI 기획 및 구현, ERD 설계
  - 신민하: 영화정보 구현(영화 API 활용), 게시판 UI/UX 구현
  - 신수인: 메인 홈페이지 UI 및 로그인/회원가입 구현, 회원정보 수정 구현, 권한별 기능 구현
  - 임지선: 상영예정작 API를 활용하여 정보 구현, 메인 UI/UX 기능 구현, 영화상세정보 메뉴 기능 구현
  - 이도민: 공지사항 게시판 CRUD 구현, 댓글 구현, 영화정보 UI 구현
  - 심기훈: 영화정보의 평점 및 댓글 구현, 영화정보 UI/UX 구현, 공지사항 CRUD 구현
  - 김보성: 영화정보 UI 및 개발, 유지보수, 영화정보 UI/UX 구현
  - 박다진솔: 검색페이지 구현, 검색결과에서 영화 상세정보 이동 구현

* 구현 기능

 * DB ERD 설계
![image](https://github.com/brandmin/HueFlix/assets/82518048/450f63a7-0d91-4fca-893f-fadbea434093)

--------------------
# 📝 구현기능

## 메인 홈페이지
![image](https://github.com/brandmin/HueFlix/assets/82518048/12658844-1db0-4364-9440-291bcccb4bc3)

* 설명
  - 영화를 슬라이드로 배치되어 있는 페이지입니다. (Swiper 라이브러리 사용)
  - 영화DB는 TMDB 사이트의 API입니다.
  - JavaScript Ajax함수를 사용하여 TMDB API의 데이터를 요청하였음.
  - API에서 반환한 JSON형식의 데이터를 받아와 처리하였음.

## 회원가입, 로그인
![image](https://github.com/brandmin/HueFlix/assets/82518048/3a78ea54-29f1-435f-b242-81416b8d6842)
![image](https://github.com/brandmin/HueFlix/assets/82518048/c5c9a1cb-9e0f-4e53-9d12-e7774dd59032)

* 설명
  - 사이트를 이용하기 위한 회원가입과 로그인 화면.
  - 회원가입은 유효성 검사를 거쳐 진행(Spring Security)


## 정보 수정(1)
![image](https://github.com/brandmin/HueFlix/assets/82518048/9551dbb9-4bb6-4f46-a8b8-1bfe33af3047)
![image](https://github.com/brandmin/HueFlix/assets/82518048/a370adc1-0a87-4fbe-b66d-16411a532824)
![image](https://github.com/brandmin/HueFlix/assets/82518048/5c59cdc7-03e2-42f5-b999-457256042638)

* 설명
  - 사용자의 정보를 수정하기 전 비밀번호를 입력하는 페이지입니다.
  - 유효하지 않은 비밀번호를 입력하면 경고메시지를 띄움

## 정보 수정(2)
![image](https://github.com/brandmin/HueFlix/assets/82518048/b2382736-097e-479e-891e-2c13ba186f2c)
![image](https://github.com/brandmin/HueFlix/assets/82518048/74705d9c-86ff-4302-a19e-284e21c83d70)

* 설명
  - 닉네임, 비밀번호를 변경할 수 있는 페이지.
  - 유효하지 않은 비밀번호를 입력했을 경우 수정할 수 없도록 구현




