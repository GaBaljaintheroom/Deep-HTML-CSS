# Deep-HTML-CSS
<h2>Practice02번 - 그리드 레이아웃</h2>


<h3> style02.css - 주요 코드</h3>

1. grid-template 속성으로 행과 열 사이즈 나누기(부모 적용 속성)
    - grid-template-columns: 200px 1fr 300px;
    - grid-template-rows: 80px 200px auto 200px;
2. 자식 요소들 사이즈 정하기
    - grid-column: 1/-1;
    - grid-row: 2/4;
    
<i>크롬 개발자 도구로 grid 속성확인해보며 코딩하기</i>

<h2>Practice03번 - 변형과 애니메이션</h2>


<h3> style03.css - 주요 코드</h3>

1. 마우스 커서를 올려 넣을시 색 및 가장자리 자연스럽게 변화
    - transition 1s;
2. 마우스 커서를 올려 넣을시 박스의 크기가 순간적으로 커졌다 되돌아옴
    - @keyframes --> transform: scale();{요소를 확대 축소}
3. 오른쪽으로 파란박스 계속 이동 
    - transform: skeywX(-30deg) 요소를 비튼다
    - animation-duration: 2s;   애니매이션 가동 시간 지정
    - animation-timing-function: linear;    동일한 속도로 애니매이션 가동
    - animation-iteration-count: infinite;  애니매이션 횟수 무한반복

<b>transiton 속성</b>

CSS 값이 달라질 때 요소에 어떤 효과로 반영될지 지정합니다.
속성, 지속시간, 시간함수, 지연시간 순으로 값을 넣을 수 있습니다.

<b>@keyframes 속성</b>

개발자가 애니메이션 중간중간의 특정 지점들을 거칠 수 있는 키프레임들을 설정함으로써 CSS 애니메이션 과정의 중간 절차를 제어할 수 있게 합니다. (from -> 50% -> to)

<h2>Practice04번 - 
그리드 레이아웃을 반응형 웹으로 크기에 따라 aside의 위치와 메뉴, nav바가 달라짐</h2>


<h3> style04.css - 주요 코드</h3>

1. 반응형 웹 페이지 
    - 스마트폰, pc에 적합하게 @media로 최대 너비와 최소 너비를 나눔
2. 화면이 클 때는, menu가 안보임 
    - #menu{ display: none;}
   aside, main의 너비 및 길이를 지정  
    -  grid-template-columns: 200px 1fr;
    -  grid-row: 2/3;
   header, footer가 grid-column속성으로 너비를 꽉채움
    - grid-column: 1/-1;
3. 화면이 작을 때는, nav바 안보임
    - nav{ display: none; }
4. menu에 마우스 갔다대면 nav바 보임
   - #menu:hover + nav{ display: inherit; }
5. nav바 오른쪽으로 블록 형식으로 정렬


<h2>Practice05번 - 
반응형 웹으로 사진은 어느 정도만 넘겨도 자동으로 넘겨지는 기능</h2>


<h3> style05.css - 주요 코드</h3>

1. 반응형 웹 페이지 
    - 스마트폰, pc에 적합하게 @media로 최대 너비와 최소 너비를 나눔
2. 하나의 사진이 뷰포트에 꽉차보이게함
    - height: 100vh;
3. container안에 div 자식들이 놀아 다닐 수 있게 함
    - overflow-y: scroll;
4. 사진을 어느 정도만 넘겨도 자동으로 다음 사진으로 넘어가짐
    pc버전은 y축 기준이고 모바일 버전은 x축 기준으로 됨 --> scroll-snap-type: x mandatory;
    - (contain)scroll-snap-type: y mandatory;
    - (div)scroll-snap-align: start;
5. 모바일 버전에서는 사진의 크기가 가로 세로 비율을 1대1로 함 
    - aspect-ratio: 1;
    


<b>미디어 쿼리(@media)</b>

단말기의 유형(출력물 vs. 화면)과, 어떤 특성이나 수치(화면 해상도, 뷰포트 너비 등)에 따라 웹 사이트나 앱의 스타일을 수정할 때 유용합니다.

<b>벤더 프리픽스 (-webkit-backdrop-filter:)</b>

아직 CSS 권고안에 포함되지 못한 기능이나, CSS 권고안에는 포함되어 있지만 아직 완벽하게 제정된 상태가 아닌 기능을 사용하고자 할 때 벤더 프리픽스를 사용하게 됩니다.
그렇게 하면 해당 기능이 포함되어 있지 않은 이전 버전의 웹 브라우저에서도 그 기능을 사용할 수 있게 됩니다.

 <b>backdrop-filter속성</b>
 
 포토샵 같은 기능 - 벤더 프리픽스와 같이 사용함 ( 사파리에서도 사용하기 위해 )
 
