# 넷플릭스 클론코딩

## 만들게 될 넷플릭스 사이트

![Untitled](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/b7e9c35f-59dc-4c22-ae08-b6d343369469)

## 만든 웹사이트

![Untitled 1](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/a692ea56-113b-4f56-aaf7-c07d9794ac83)

![Untitled 2](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/548f6ec8-5ebe-4aff-9ffc-85fb3c6ad8bc)

## html 구조

![Untitled 3](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/7f717c75-6e62-43c2-aeea-89d7813e4c97)

## 요구사항 정리

### nav

- [backgroundImg](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/nav.css#L20)
    - 맨 뒤에 배치 되고 nav에 간섭없도록
        
        absolute와 z-index 활용.
        
- [nav-top](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/nav.css#L30)
    - 넷플릭스 logo, user icon 양 끝에 배치하기 위해 flex-box를 이용
- [nav-bottom](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/nav.css#L42)
    - main-movie-name : 메인 영화 이름
    
    - movie-buttons(2개의 버튼 포함)
        - 기능은 흐리게 효과를 구현하기 위해 rgba에 alpha 속성을 0.5로 주었음.
        - Play
        - MyList
    - main-movie-info : [영화 설명](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/nav.css#L77C10-L77C10)
        - overflow: hidden;
        - display: -webkit-box;
        - -webkit-line-clamp: 3;
        - -webkit-box-orient: vertical;
        - text-overflow: ellipsis;
        - 요약 : webkit-box를 이용해서 영화 부연 설명이 3줄이 넘어갈 시 … 이라는 효과를 주고 overflow 된 글을 숨기는 효과를 주었다.

### Section

- [section-title](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/section.css#L8)
    - nextflex Originals 라는 단어를 적음
- [section-movies](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/section.css#L14)
    - 8가지의 movie를 flex 라는 속성을 이용해서 배치
    - p > img 를 넣어주어 img에 호버할 시에 이미지가 커지는 효과를 주었다.
        - 구현이유
            
             처음엔 p태그가 없었는데 hover할시에 이미지가 변동이 안됐다 내가 생각하기엔 section-movies 를 display : flex 속성으로 flex-direction : row 로 설정하여서 제어가 안되었던 것 같다. p 태그를 넣어서 해결함.
            

### footer

- [footer-title](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/footer.css#L8)
    
    Tranding New라는 제목이 부여됨.
    
- [footer-moives](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/577f44ed6a2b47a47271eefcbc9fa79c00bffbff/styles/footer.css#L15)
    
    footer-movies 에는 총 8가지 img 태그가 존재하고 flex로 구현함.
    

## 조건

- 1. flex-box 이용하기
    - nav-top, nav-bottom, section, section-movies, footer, footer-movies
    - 총 6군데 사용

- 2. 영화포스터에 마우스로 호버하면 영화포스터의 사이즈가 크게 될 수 있도록
    - section > moive를 hover할 시에 이미지가 0.3동안 천천히 이미지가 커지도록 설정하였음.
