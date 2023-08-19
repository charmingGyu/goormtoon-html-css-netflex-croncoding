# 넷플릭스 클론코딩

## 만들게 될 넷플릭스 사이트

![Untitled4.png](%E1%84%82%E1%85%A6%E1%86%BA%E1%84%91%E1%85%B3%E1%86%AF%E1%84%85%E1%85%B5%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A9%E1%86%AB%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B5%E1%86%BC%204727800c47a843bb97f7a0bd7ed8897e/Untitled4.png)

## 만든 웹사이트

![Untitled](%E1%84%82%E1%85%A6%E1%86%BA%E1%84%91%E1%85%B3%E1%86%AF%E1%84%85%E1%85%B5%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A9%E1%86%AB%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B5%E1%86%BC%204727800c47a843bb97f7a0bd7ed8897e/Untitled.png)

![Untitled](%E1%84%82%E1%85%A6%E1%86%BA%E1%84%91%E1%85%B3%E1%86%AF%E1%84%85%E1%85%B5%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A9%E1%86%AB%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B5%E1%86%BC%204727800c47a843bb97f7a0bd7ed8897e/Untitled%201.png)

## html 구조

![Untitled](%E1%84%82%E1%85%A6%E1%86%BA%E1%84%91%E1%85%B3%E1%86%AF%E1%84%85%E1%85%B5%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A9%E1%86%AB%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B5%E1%86%BC%204727800c47a843bb97f7a0bd7ed8897e/Untitled%202.png)

## 요구사항 정리

### nav

- [backgroundImg](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/3278befa038f1c7f6b7353db8a808967eb5d146a/styles/nav.css#L19)
    - 맨 뒤에 배치 되고 nav에 간섭없도록
        
        absolute와 z-index 활용.
        
    - 아래로 흐리게 하는 효과 추가
        - before
- [nav-top](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/3278befa038f1c7f6b7353db8a808967eb5d146a/styles/nav.css#L40)
    - 넷플릭스 logo, user icon 양 끝에 배치하기 위해 flex-box를 이용
- [nav-bottom](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/3278befa038f1c7f6b7353db8a808967eb5d146a/styles/nav.css#L51)
    - main-movie-name : 메인 영화 이름
    
    - movie-buttons(2개의 버튼 포함)
        - 기능은 흐리게 효과를 구현하기 위해 rgba에 alpha 속성을 0.5로 주었음.
        - Play
        - MyList
    - main-movie-info : [영화 설명](https://github.com/leebongseung/goormtoon-html-css-netflex-croncoding/blob/3278befa038f1c7f6b7353db8a808967eb5d146a/styles/nav.css#L87C12-L87C12)
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
