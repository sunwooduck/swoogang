# 수강신청 시뮬레이터 :desktop_computer:

------

## ![imge](https://img.shields.io/badge/ProjectType-TeamProject-green) ![imge](https://img.shields.io/badge/Language-Java-yellow) ![imge](https://img.shields.io/badge/Tools-intelliJ-blue)

## 프로그램 소개 :thumbsup:

- 대학 생활을 하면서 느낀 수강신청의 불편함을 해결하기 위해 만든 수강신청 시뮬레이터 입니다.
- 검색 구분의 범위가 넓어 원하는 강의에 한번에 접근하기 어려운 것과 겹치는 시간대를 일일이 확인해야하는 불편함등 다양한 불편함을 해결하였습니다.
- 서버와 연결되어 Stand-alone 모델에서 Sever-Client모델로 기능이 분리되어있습니다.  
- 사전 설정
  - libs의 **mail.jar, activation.jar, additionnal.jar, json_simple-1.1.jar**을 라이브러리에 추가해야 사용이 가능합니다.
  - Controller의 SignUpController의 130번 줄과 131번 줄에 자신 이메일의 ID와 PW를 입력해야 사용이 가능합니다. (보안 설정은 따로 하셔야합니다.)

## 주요 기술 요소

### 객체지향의 개념 적용

- 클라이언트와 서버로 메인 프로그램을 분리하고, 프로그램을 구성하는 클래스는 객체지향 프로그래밍 기법에 따라 세분화시키고 계층화함.
- 추상 클래스, 상속, 오버로딩, 오버라이딩 등을 직간접적으로 적용 및 구현.

### MVC패턴 도입

- GUI 프로그램의 기본 프로그래밍 모델인 MVC패턴을 적용.

### 싱글턴 기법 적용

- 메모리 절약 및 객체지향의 기능을 활용해 싱글턴 기법을 적용.

## 전체 시스템 구조도

![시스템구조도](https://user-images.githubusercontent.com/37828448/71703519-4df1b380-2e18-11ea-8115-805fc0ee20b6.png)

------

## 프로그램 UML :building_construction:

![UML](https://user-images.githubusercontent.com/37828448/71703577-ad4fc380-2e18-11ea-85d5-8a154ab9c1f3.png)



------

## 프로그램 기능소개

|      기능 명       |                          기능 설명                           |
| :----------------: | :----------------------------------------------------------: |
| 로그인 및 회원가입 |               학번으로 회원가입 후 로그인 가능               |
|      수강신청      | 필터기능을 통해 원하는 과목을 필터링하며, 수강신청이 가능함  |
|     시간표보기     | 자신의 시간표를 PDF파일로 출력이 가능하며, 시간표로 볼 수 있음 |
|     학점 계산      |         신청된 과목을 기반으로 학점계산을 할 수 있음         |

- 모든 기능은 서버와 연동되어 동작한다.
- 수강 신청 시, 강의를 자동으로 계산하여 신청이 불가능한 강의를 빨간색으로 표시됨.

### 로그인

![회원가입](https://user-images.githubusercontent.com/37828448/71665237-72f61000-2d9f-11ea-8429-80d8eebf282c.gif)

- 이메일 인증 기능 구현
- ID중복 확인 기능 구현

### 메인화면

![image](https://user-images.githubusercontent.com/37828448/71543853-529f0d80-29bb-11ea-9564-0923c59a20c7.png)

- 메인화면으로 엑셀파일을 불러오며 각 화면으로 이동 가능.
- 엑셀파일은 apache library를 활용해 읽음.

### 수강신청 필터

![image](https://user-images.githubusercontent.com/37828448/71543862-706c7280-29bb-11ea-9faa-dc69e9e3c1e1.png)

- 각 필터를 적용시켜 원하는 과목만 읽어올 수 있음.

### 수강신청

![수강신청](https://user-images.githubusercontent.com/37828448/71665198-4e9a3380-2d9f-11ea-8460-189b167fa6c6.gif)

- 실제 수강신청과 동일하게 정보 제공
- 자신이 신청한 과목과 동일한 과목이거나, 시간이 겹치는 경우 빨간색 글씨로 신청이 불가능한 것을 표현. (신청을 누르면 에러 메세지가 뜸)
- 현재 수강신청 인원 확인 가능 (새로고침)

### 시간표 보기

![image](https://user-images.githubusercontent.com/37828448/71305039-a20c9900-2411-11ea-8ff8-ce7e5b4c6246.png)

- 자신의 수강신청한 과목을 바탕으로 시간표를 볼 수 있습니다.

### 학점 계산기

![image](https://user-images.githubusercontent.com/37828448/71543867-8ed26e00-29bb-11ea-8700-6f1d0f8793f9.png)

- 수강신청한 과목을 바탕으로 학점을 계산해 줌. 추가로 적을 수 있다.
