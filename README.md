# ⭐️Portfolio - HueFlix

 <!-- contents -->
<details>
  <summary>
    Content
  </summary>


  - [ 개요](#개요)
  - [ 내용](#내용)
  - [ 구현기능](#구현기능)
  - [ 프로젝트하면서 아쉬웠던 점](#프로젝트하면서-아쉬웠던-점)
</details>

-----------
# 📝개요
* 프로젝트 명: HueFlix

* 일정: 2023년 12월 4일 ~ 2023년 12월 22일

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
# 📝구현기능

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
<br>
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


## 메뉴-현재상영작, 개봉 예정작
![image](https://github.com/brandmin/HueFlix/assets/82518048/b47f90fd-28e6-4d69-a307-3f10fc303f2a)
![image](https://github.com/brandmin/HueFlix/assets/82518048/7db9fd51-8b9f-4971-9617-fadd353048b6)

* 설명
 - TMDB API key를 통해 현재상영중인 최신 영화정보를 받아와 표시
 - 영화 포스터를 클릭하면 해당 영화상세정보 이동

## 게시판(일반 로그인 상태)
![image](https://github.com/brandmin/HueFlix/assets/82518048/365fb255-04b5-49cd-afd2-3e5434822931)

* 설명
 - 게시판 읽기와 키워드 검색이 가능한 게시판.
 - 1페이지에 게시글 10개가 출력되도록 구현(페이지네이션)

## 게시판(일반 사용자 읽기)
![image](https://github.com/brandmin/HueFlix/assets/82518048/1aa6270a-2681-43b7-a67b-ab71c1885641)

* 설명
 - 일반 사용자는 게시판 내용을 수정, 삭제할 수 없음.
 - 목록보기 버튼을 누르면 게시판 목록 이동

## 게시판(관리자 로그인 상태)
![image](https://github.com/brandmin/HueFlix/assets/82518048/2292f5f7-f3de-4b9a-a0a8-0497bcf1fcfb)

* 설명
 - 게시판 작성, 키워드 검색이 가능한 게시판
 - 제목을 누르면 해당 읽기 페이지로 이동

## 게시판(관리자 읽기)
![image](https://github.com/brandmin/HueFlix/assets/82518048/f5f7aae1-f248-4d24-ad92-4b71c258714f)

* 설명
 - 게시판 관리자는 수정, 삭제 권한을 부여하여 CRUD가 가능한 게시판
 - 목록보기 버튼을 누르면 게시판으로 이동

## 영화 상세정보
![image](https://github.com/brandmin/HueFlix/assets/82518048/722f4f88-b261-4cff-9bb2-20c9963d3d73)
![image](https://github.com/brandmin/HueFlix/assets/82518048/ca984571-feb6-41c5-b9b0-b15697f934ec)
<br>
![image](https://github.com/brandmin/HueFlix/assets/82518048/b5d86ea4-260c-4011-b337-fe592b846a99)
![image](https://github.com/brandmin/HueFlix/assets/82518048/006146c9-046d-4696-8f43-fe165552f62f)

* 설명
 - 특정 영화 아이디 값을 활용하여 API를 호출하며 이를 통해 해당 영화의 줄거리, 출연, 영상/포토, 평점/댓글을 표시하는 페이지
 - 사용자의 평점 및 댓글은 댓글 작성시 별 모양 버튼을 누르면 평점을 추가하고 영화 관련된 내용을 평가할 수 있음.
 - 관리자 권한을 가진 아이디는 사용자의 댓글을 삭제할 수 있음.
 - 일반 사용자 권한을 가진 아이디는 자신이 작성한 댓글만 삭제할 수 있음.

## 영화, 영화인 검색
![image](https://github.com/brandmin/HueFlix/assets/82518048/6a57b1d8-1c1c-4bcd-b4b4-be4312acba24)

* 설명
 - 검색창의 입력문자열을 검색 API를 통해 각 영화, 영화인을 검색할 수 있음.
 - 검색결과에 출력되는 영화 포스터를 클릭하면 해당 영화상세정보로 이동

---------
# 📝프로젝트하면서 아쉬웠던 점
제가 맡았던 게시판의 CRUD기능과 댓글에서 Spring Security을 사용하여 일반 사용자 혹은 관리자 권한을 줄 수 있는 기능을 구현하지 못하였습니다.
그래서, Security 부분에 대해 다시 한번 더 학습하고 이후 프로젝트에 적용해볼 계획입니다.

그리고, 게시판을 작성했을때 해당 게시글의 파일을 업로드할 수 있는 기능을 구현하지 못하였습니다. 따라서, 이 부분의 파일 업로드 구현을 Ajax 함수를 사용하여 구현해볼 계획이고 이 부분도
유튜브 강의를 참고하여 적용하려고 합니다.













