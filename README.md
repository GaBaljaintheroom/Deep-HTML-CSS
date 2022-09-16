# Deep-HTML-CSS

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
 
