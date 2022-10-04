
<img src="https://user-images.githubusercontent.com/107850055/193414162-50692ac0-337e-43db-a2e9-54b6b3da7e43.gif"></img>
<!-- 1.첫번째 오류 : local storage에 저장한 데이터들을 map을 사용해서 값을 불러오려고 했는데 Uncaught TypeError: memolist.map is not a function 오류가뜸. 이유는 내가 로컬 스토리지에 데이터를 저장할때 배열 형태로 저장한게 아닌,string으로 저장했기 때문에 배열로 이루어진 data에만 처리가 가능한 map이 작동하지 않아서 생긴 오류였고 배열형태로 데이터를 저장해주니까 정상작동됐다.
2.두번째 오류 : create버튼을 누르게되면 입력된 데이터가 바로 local storage로 저장이 돼야 하는데 클릭을 두번해야 데이터가 저장이 됐다. -->
<h2>💖 만들게 된 계기</h2>
<p>부트캠프 Section3 솔로 과제를 생각하던 중 여태까지 안해봤던 기능들을 구현해보고 싶어서 만들게 되었다. 자바스크립트나 리액트를 이용해서 To-Do-list는 여러번 만들어 봤지만, Search기능과 수정하기 기능은 한번도 구현해본적이 없었기 때문에 시도해봤다.  </p>
<h2>💎 업데이트 예정</h2>
<p>1. 가독성을 위해 CSS 수정하기<br>
2. 메모 리스트 시간순으로 정렬하기
3. 삭제버튼 클릭시 모달 페이지 띄우서 한번 더 확인하기
</p>
<h2>💡 세부 기능</h2>
<h3>Search</h3>
찾고자 하는 메모장의 내용을 input창에 입력하게 되면 그에 맞는 메모리스트들을 출력하는 기능을 구현하였다.

<h3>Note Read 및 Update</h3>

작성한 메모들의 내용과 작성 당시 시간을 보여주고, 작성한 메모 수정시 새로운 데이터로 업데이트 되도록 구현하였다.

<h3>Memo 작성 / 수정 / 삭제</h3>
 
Note 작성시 localstorage의 해당 메모에 해당하는 key값을 value값과 useNavigate를 활용하여 만든 변수 navigate 전달해 해당 메모페이지 주소에 key값을 추가하여 주소를 생성하도록 했고, 이 주소를 useParams와 useNavigate를 활용해 조회 및 수정이 가능하도록 구현하였다. 메모 수정시 작성시간을 새로 업데이트하여 페이지의 key값을 변경하고, 기존에 작성되어 있던 Note를 삭제하고 새로운 값을 생성하는 방식으로 기능을 구현하였고, 삭제 기능은 localStorage.removeItem 메서드와 Note값 Read시 사용되었던 map함수의 매개변수 item을 props로 전달받아 삭제하도록 구현하였다.








