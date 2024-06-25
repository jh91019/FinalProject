# 🏨 숙박 예약 웹 사이트
국비 훈련 과정에 진행한 최종 팀 프로젝트입니다.
3개 이상의 역할이 명확하게 구분되는 사이트, 사용자 간의 상호작용이 이루어지는 사이트, 다양한 API를 활용할 수 있는 사이트를 만들고자 주제를 선정하였습니다.

<br/>

* * *

## 📑 목차
[1. 프로젝트 개요](#1-프로젝트-개요)
  - [개발 기간](#-개발-기간)
  - [주제 및 목표](#-주제-및-목표)
  - [사용 기술](#-사용-기술)
   
[2. 프로그램 구조 및 구현 기능](#2-프로그램-구조-및-구현-기능)
  - [ER Diagram](#-er-diagram)
  - [팀원별 구현 기능](#-팀원별-구현-기능)

[3. 주요 구현 기능 설명](#3-주요-구현-기능-설명)
  - [호스트 회원가입 및 승인](#-호스트-회원가입-및-승인)
  - [호텔 등록 및 영업 관리](#-호텔-등록-및-영업-관리)
  - [숙박 예약 및 예약 관리](#-숙박-예약-및-예약-관리)
  - [후기 및 평점 관리](#-후기-및-평점-관리)

[4. 후기 및 개선점](#4-후기-및-개선점)
  - [프로젝트 후기](#-프로젝트-후기)
  - [개선점](#-개선점)

<br/>

* * *

## 1. 프로젝트 개요
### 📅 개발 기간
2024.04.24 ~ 2024.06.05 (약 6주)
- 1주차 : 주제선정 및 프로젝트 기획회의. DB설계. 개발환경 세팅.
- 2~3주차 : 개인별 집중 개발 진행 후 1차 통합테스트 진행.
- 4주차 : 세부기능/추가기능 등 피드백 후 수정 작업 진행.
- 5주차 : 2차 통합테스트 및 오류 수정.
- 6주차 : 발표자료 및 프레젠테이션 준비. 6/11 최종시연.

<br/>

### 📝 주제 및 목표
**[주제]** : 숙박 예약 웹 사이트 
**[목표]**
1. DB 구축 및 SQL 연습
2. 직관적인 UI/UX 구성
3. Spring MVC 패턴 적용
4. 다양한 라이브러리 활용 및 적용

<br/>

### 💻 사용 기술
**[사용 기술 및 개발 환경]**
- OS : Windows11
- Front-end  : HTML/CSS, React, Javascript
- Back-end :  Java(JDK21), Spring Framework, MariaDB 11.3
- Tools : Spring Tool Suite 4, Heidi SQL 12.6, Git, Sourcetree, Draw.io
- Library : Lombok 1.18.30, MyBatis 3.5.15, Bootstrap 5.3, Sweetalert2, Chart.js 4.4.0 etc.

<br/>

* * *

## 2. 프로그램 구조 및 구현 기능
### ☑ ER Diagram
![erd](https://github.com/jh91019/FinalProject/assets/156145497/8a5d8ce4-f4c5-484e-b8bb-bc85714969d6)

### ☑ 팀원별 구현 기능
![팀원별](https://github.com/jh91019/FinalProject/assets/156145497/4c30916f-71ea-4f98-9d25-684243d7895f)

<br/>

* * *

## 3. 주요 구현 기능 설명
### 📜 호스트 회원가입 및 승인
![approve](https://github.com/mindyhere/final-project/assets/147589193/153b76b9-3528-43aa-8bff-5e3f159fcc33 "flow1")
- 호스트 회원가입
  -  각 항목마다 필수 입력 Alert 표시
  -  이메일 유효성 확인 → 중복확인 버튼 활성화 → 사용가능한 이메일에 한해 회원가입 가능
![호스트 회원가입 영상](https://github.com/mindyhere/final-project/assets/147589193/570ed74d-b23d-4676-8d89-33188b9eb6e8)
- 호스트 승인요청
  -    최초 가입 시 “가입 완료” 상태 → 호스트 승인요청 시, 첨부파일 등록 필수(프로필/사업자 등록증/ 통장사본) → 승인요청 버튼 활성화
  - [승인요청] 클릭 시 완료 Alert
- 관리자 - 호스트 가입 승인
  - 신규 회원 승인 대기 상태일 때 [가입승인] 버튼 클릭 후, 사업자등록증, 통장사본 일치 확인 가입정보 일치 → 승인 완료 Alert
![approve1](https://github.com/mindyhere/final-project/assets/147589193/05c332cc-e66b-4257-9113-a34c66fcac6b)

<br/>

### 🏨 호텔 등록 및 영업 관리
![hotel](https://github.com/mindyhere/final-project/assets/147589193/77fc6c98-8df6-4189-a236-e93a445f5236 "flow2")
- 호텔 신규등록
  - 기본정보 입력 후 ‘다음’ 클릭 시 편의시설, 객실정보 입력하는 페이지로 이동
  - 객실 정보 등록 시, 싱글룸은 필수 입력, 객실 사진은 최대 3장까지 첨부 가능
![숙소 등록하기](https://github.com/mindyhere/final-project/assets/147589193/6aa97fe5-4d82-4543-8845-b4f34218ac4c)
- 호텔 등록 : 이어서 작성하기 기능 적
  -  작성 중인 내용이 있을 경우 이어서 작성할 것인지 묻는 Alert
  -  "네” 선택 : 입력했던 데이터 불러온 후 이어서 작성 가능 / “아니오” 선택 : 저장되었던 데이터 삭제, 신규 데이터 입력
![신규호텔_이어서](https://github.com/mindyhere/final-project/assets/147589193/50d8226d-7e40-471e-80c1-4e9a51787a0c)
- 숙소영업관리 및 숙소승인
  - 신규등록호텔이 “승인대기” 상태일 때 → [승인] 버튼 클릭 → “영업중” 상태로 변경
![호텔 등록 승인](https://github.com/mindyhere/final-project/assets/147589193/9af3c403-4cb6-4474-b5ac-41d0bd6ec5dc)

<br/>

### 📇 숙박 예약 및 예약 관리
![reservation](https://github.com/mindyhere/final-project/assets/147589193/5b56dafe-191c-49da-a502-8b3c7d65761d "flow3")
🔗 [숙박예약/결제 시연영상 보기](https://github.com/mindyhere/final-project/assets/147589193/cbf80039-e428-42be-ae34-cf464309f211)
- 포트원API 및 카카오페이 결제API 적용

![ex2](https://github.com/mindyhere/final-project/assets/147589193/4c2f9745-e179-4940-8ad4-893273566ea0)
![ex5](https://github.com/mindyhere/final-project/assets/147589193/8c010fce-1a43-4707-88cd-41238e620c53)
- 호스트 예약관리 : 예약확정/체크인완료 처리 또는 예약변경 승인/거부 처리 → 예약확정 시 바우처 이메일발송

<br/>

### 📝 후기 및 평점 관리
![reputation](https://github.com/mindyhere/final-project/assets/147589193/f4615140-0746-493b-b973-c18ecb8b512d "flow4")
![reputation1](https://github.com/mindyhere/final-project/assets/147589193/e752f61c-0bed-4d99-b36d-eae9c604c754)

- 게스트
  - 리뷰가 등록되어 있지 않은 지난 여행만 작성 가능 
  - 프로필에서 본인 작성 리뷰 조회 및 수정, 삭제 가능 
  - 호스트가 남긴 답글 조회 가능
- 호스트
  - 해당 호텔의 별점 및 리뷰 상세 조회 가능
  - 답글 등록, 수정, 삭제
- 호텔 상세페이지, 평점 및 후기란에서 조회 가능
  
<br/>
<br/>

__※ 상세 기능은 [발표 자료](https://docs.google.com/presentation/d/17xhSXil2K-h7-_tIEPv6zsKwHZvXYaMbxjTMpMjHYV8/edit?usp=sharing)에서 더 보실 수 있습니다.__

* * *
 
## 4. 후기 및 개선점
### 🖍 프로젝트 후기
- Github를 활용하여 원활한 팀 프로젝트를 진행할 수 있었다.
- 안드로이드를 활용한 숙박 예약 어플, 관리자-호스트 매출/정산 기능 등 기획 단계에서 더 많은 아이디어가 나왔었는데 여건상 시도하거나 최종 구현하지 못한 부분들이 아쉬움으로 남는다.
- 프로젝트 기획 과정에서 다양한 테이블 관계 형성과 프로시저, 새로운 프론트엔드(React)를 활용할 수 있도록 노력했고 그 결과 많은 공부가 되었다. 
- 팀 프로젝트를 통해 많이 배우고 부족한 부분을 채워 성장할 수 있는 계기가 되었다.

<br/>

### ⚒ 개선점
- 깜박임 현상이 잦아 아쉬움. 후 axios(비동기 처리)로 개선 필요.
- 관리자 자동 로그인 기능 추가.
- 후기 작성 후 일정 기간이 지나면 수정/삭제가 불가능하도록 개선 필요.
- 호스트 가입 승인 시 가입 정보가 일치하지 않으면 ‘승인 요청 거부’ 메시지가 전달되도록 개선 필요.
