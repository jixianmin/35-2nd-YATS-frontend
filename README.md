# 2차 프로젝트 "Oil Of Yats"

## 팀소개

팀명 : YATS / OIL OF YATS
팀원 : FE - 길현민, 김수정, 주원영, 최재홍 / BE - 이정훈, 성바울, 홍현진

## 프로젝트 소개

스테이폴리오(STAYFOLIO)는 머물고 싶은 집을 뜻하는 “STAY”와 관점을 갖고 큐레이팅하여 차곡차곡 모아둔 2절판의 책 “FOLIO”의 합성어로서 어원이 지니는 의미 그대로 머물고 싶은 좋은 스테이를 큐레이팅하여 소개하는 웹진입니다.

## 필수 구현 사항

1. 메인페이지
2. 로그인 (OAuth2.0) - 카카오
3. Find Stay - 숙소 리스트 (정렬, 필터,페이지네이션)
- query parameter를 이용한 카테고리별 데이터 호출
- kakaomap API 지도를 불러옵니다
- 카테고리 검색후 해당 상품 수량에 맞게 백엔드 해당 페이지네이션 데이터를 전송해줍니다.
- 백엔드 API는 해당하는 데이터들을 전송해준다.

pagenation 및 sort 기능 구현
- page당 상품 갯수(limit) 버튼을 추가해 사용자가 값을 입력하면, 이 값을 API endpoint로 전달한다.
- 이때 API로부터 전체 상품 갯수(total)를 전달받아, total과 limit을 사용해 전체 페이지 수를 구한다.
- 전체 페이지수를 기준으로 페이지네이션 로직을 구현하고, 페이지 수를 클릭할 때마다 이값도 API에 전달해준다.
- 백엔드 API는 limit, page, category 값을 받아 해당하는 데이터리스트를 전송한다.
- 다른 검색순을 추가해 사용자가 값을 입력하면 백엔드와 약속한 string을 API에 보내준다.
- 백엔드 API에서 해당하는 정렬 순서로 데이터리스트를 보내준다.

query parameter를 이용한 카테고리별 데이터 호출
- 카테고리 메뉴탭을 클릭하면 url에 ?category={number}의 형식으로 나타나게끔 로직을 구현하고
- searchParams를 이용해 category 값을 받아 API의 endpoint로 요청한다.
- 백엔드 API는 해당하는 데이터들을 전송해준다.

검색 기능 구현
- 사용자가 검색창에서 값을 입력하면 그 값을 담은 url로 이동하도록 로직을 구현했다. (navigate(/Search?keyword=${searchValue});)
- 사용자가 입력한 검색값을 query parameter를 이용해 API에 보내주고, 응답받은 필터된 데이터 리스트를 화면에 구현

4. 숙소 상세 페이지 (예약 하기) + 네이버 Map
5. 입점 문의

## 작업기간,구현기능,사용기술 소개
- 작업기간 2022/08/01 ~ 08/12 약 2주간의 기간동안 작업했습니다.

- 구현기능: 숙박업체의 기본적인 FLOW를 갖추고 있습니다.

- 사용기술 
  Front-end: HTML, Styled Components, Javascript, React
  Back-end: Phython, Django, MySQL, AWS-RDS S3

## 프로젝트 협업 도구
### 1.Trello
- 기능 단위로 카드를 생성하여 프로젝트가 sprint 미팅대로 잘 이루어졌는지 파악하고 stand up 미팅 활용한 도구로 활용
### 2.Slack
- 팀원간의 실시간 소통 창구

## 프로젝트 회고
- 아쉬웠던점
- 잘했던점
