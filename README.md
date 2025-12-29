# [reste]
> [가구 쇼핑몰 사이트]

## 1. 프로젝트 소개
* **설명:** 기획과 디자인, 장바구니 페이지 개발에 참여하였고 **Mock Data(JSON)**를 활용해 실제 커머스 로직을 구현한 RESTE 쇼핑몰 프로젝트입니다.
* **진행 기간:** 2025.12.22 ~ 2025.12.29 (8일)
* **개발 인원:** FrontEnd 5인 (Team Project)
* **배포 링크:** https://daehyeonkim0326-sys.github.io/reste/

## 2. 사용 기술 스택 (Tech Stack)
* **Language:** JavaScript (ES6+)
* **Framework:** React.js
* **Styling:** SCSS
* **Data Handling:** Custom Mock Data (JSON)
* **Design & Tool:** **Figma**, Git, GitHub, VScode,GSAP,reactbits,photoshop

## 3. 기획 및 디자인 (Planning & Design)
* **Tool:** Figma,photoshop
* **Concept:** 사용자 직관성을 고려한 UI/UX 설계 및 와이어프레임 제작

## 4. 디렉토리 구조
```text
src
├── assets        # 이미지, 폰트, JSON 데이터, scss
├── components    # 이미지 카드,팝업 등 재사용 가능한 공통 UI 컴포넌트
├── pages         # 라우팅 페이지와 style scss (MainPage, DetailPage, CartPage,ProductPage...)
└── layout        # Header,Outlet,Footer 레이아웃

## 5. 담당 역할

[기획 및 디자인]
* Figma를 활용한 전체 와이어프레임 정립과 UI설계

[개발:  기능]
*useState,useEffect,useNavigete,motion 등을 사용하여
react로 CartPage.js,CartPopup.js 컴포넌트를 만들고 scss를 활용하여 CartPage와 CartPopup style 제작  



## 6. 주요 기능
상품 데이터 처리: JSON 데이터를 활용한 비동기 통신 모방
장바구니 관리: 배열을 활용한 장바구니 추가/수정/삭제


## 7. 트러블 슈팅
문제 1.수정한 부분이 git에 업로드 되지 않는다.
상황: Compare & pull request 과정에서 수정된 코드가 git에 올라가지 않는 상황
해결:git status 로 충돌파일을 확인한 후 충돌한 지점을 수정해서 터미널에 git add src/수정한 파일 입력 후
다시 커밋하고 git push origin main 한 후에 깃허브 사이트에서 리퀘스트 
과정:git status를 사용하여 오류지점을 확인 -> 오류지점 수정 -> git add src/수정파일 터미널에 입력 -> 커밋하기 git commit -m "" -> 터미널에 git push origin main 입력 -> 깃허브 사이트에서 리퀘스트하기
문제 2.구입하기 버튼 클릭하면 상품 상세페이지로 넘어가지 않는 문제
상황: ProductMD로 Products.json에 있는 상품 id가 읽혀지지 않음
해결:MainPage.js에서 객체로 const item 으로 Products.json에서 id 찾아서 ProductMD로 Props 전달
과정: const item = products.find((p) => String(p.id) === "midnight");(MainPage.js) -> Props로 ProductMD.js에 item 전달 -> handleClick 안에 onAdd한테 item 전달 -> button을 감싸고 있는 Link에 handleClick 전달 

## 8. 실행 화면
(구현한 화면 스크린샷 1장 첨부)