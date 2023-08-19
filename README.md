# 넷플릭스 클론코딩

## 만들게 될 넷플릭스 사이트
![Untitled](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/f9179284-01a5-47a2-87a1-a59e80a4df69)



## 만든 웹사이트

![Untitled1](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/a205ff2c-f495-4699-b67c-e63ea9f73eae)

![Untitled3](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/eab10077-4682-4d57-8cb6-0315f76c2de6)

## html 구조

![Untitled4](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/assets/101985441/bc14f8de-ceb2-42f6-9ddb-be29a79c2381)

## 요구사항 정리

### nav

- backgroundImg
    - 맨 뒤에 배치 되고 nav에 간섭없도록
        
        absolute와 z-index 활용.
        
- nav-top
    - 넷플릭스 logo, user icon 양 끝에 배치하기 위해 flex-box를 이용
- nav-bottom
    - main-movie-name : 메인 영화 이름
    - movie-buttons(2개의 버튼 포함)
        - 기능은 흐리게 효과를 구현하기 위해 rgba에 alpha 속성을 0.5로 주었음.
        - Play
        - MyList
    - main-movie-info : 영화 설명
        - overflow: hidden;
        - display: -webkit-box;
        - -webkit-line-clamp: 3;
        - -webkit-box-orient: vertical;
        - text-overflow: ellipsis;
        - 요약 : webkit-box를 이용해서 영화 부연 설명이 3줄이 넘어갈 시 … 이라는 효과를 주고 overflow 된 글을 숨기는 효과를 주었다.

### Section

- section-title
    - nextflex Originals 라는 단어를 적음
- section-movies
    - 8가지의 movie를 flex 라는 속성을 이용해서 배치
    - p > img 를 넣어주어 img에 호버할 시에 이미지가 커지는 효과를 주었다.
        - 구현이유
            
             처음엔 p태그가 없었는데 hover할시에 이미지가 변동이 안됐다 내가 생각하기엔 section-movies 를 display : flex 속성으로 flex-direction : row 로 설정하여서 제어가 안되었던 것 같다. p 태그를 넣어서 해결함.
            

### footer

- footer-title
    
    Tranding New라는 제목이 부여됨.
    
- footer-movies
    
    footer-movies 에는 총 8가지 img 태그가 존재하고 flex로 구현함.
    

### 조건

- 1. flex-box 이용하기
    - nav-top, nav-bottom, section, section-movies, footer, footer-movies
    - 총 6군데 사용

- 2. 영화포스터에 마우스로 호버하면 영화포스터의 사이즈가 크게 될 수 있도록
    - section > moive를 hover할 시에 이미지가 0.3동안 천천히 이미지가 커지도록 설정하였음.
