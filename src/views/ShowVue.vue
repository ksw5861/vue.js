<!-- v-if와 v-show는 Vue.js에서 DOM 요소를 조건에 따라 보여주거나 숨기기 위한 디렉티브이다.
둘 다 true일 때만 요소를 보여주지만, 동작 방식에 큰 차이가 있다.  -->

<p v-if="isVisible">Hello!</p>

<!-- v-if 기능 설명
isVisible이 true일 때만 이 요소가 DOM에 생성됨.

false면 아예 DOM에 존재하지 않음.

즉, 조건이 false이면 아예 렌더링도 안 함. -->

<!-- 작동 방식
조건이 바뀔 때마다 DOM을 생성하거나 제거함.

초기 렌더링은 가볍지만, 토글할 때마다 DOM 조작이 일어남 → 무거울 수 있음. -->

<p v-show="isVisible">Hello!</p>

<!-- v-show 기능 설명
isVisible이 true면 보이고, false면 **보이지 않게 처리(display: none)**됨.

DOM에는 항상 존재함. -->

<!-- 작동 방식
처음부터 DOM은 만들어지고, 조건에 따라 CSS 속성으로 숨김 처리만 함.

즉, 렌더링은 되지만 화면에만 표시되지 않음. -->

<!-- 한 번만 렌더링하고 말거나, 조건이 자주 안 바뀜	 => v-if
     버튼 클릭 시 자주 보였다 숨겨야 함	            => v-show
     DOM 생성/제거로 성능에 부담 줄 수 있음	        => v-show 
     -->
