# food_study
레스토랑코드
<!DOCTYPE html>
<head>
<style>
  body {
   background-image: url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQdMu9P3s3cdJSk40ySeFy4IXjySvhMbpWMew&usqp=CAU");
   background-position: center center;
   background-size: 666px;
   background-repeat: no-repeat;
  }

  .menu-item {
   width: 200px;
   height: 250px;
   background-color: lightgray;
   margin: 10px;
   padding: 20px;
   border-radius: 5px;
   text-align: center;
  }

  .container {
   display: flex;
   flex-wrap: wrap;
   justify-content: center;
  }

  p {
   text-align: center;
  }
  
  a {
   text-align: center;
  }
  .grid-container {
   display: grid;
   justify-content: center;
   grid-template-columns: repeat(3, minmax(200px, auto));
   <!-- fr : fraction -->
   <!-- repeat(1, 2, 3, 4) -->
   <!-- 1. 몇번 반복할지, auto -->
   <!-- 2. 크기, 얼만큼 너비를 차지할지 -->
   <!-- 3,4~ 비율 -->
   <!-- minmax(최소값, 최대값) -->
   grid-gap: 20px;
  }

</style>
</head>
<body>
<h2>Flexbox Example:</h2>
<div class="container">
   <div class="menu-item">
      <h3>스테이크</h3>
      <p>완벽하게 조리된 스테이크.</p>
   </div>
   <div class="menu-item">
      <h3>파스타</h3>
      <p>선택할 수 있는 소스와 함께 신선한 파스타.</p>
   </div>
   <div class="menu-item">
      <h3>초밥</h3>
      <p>다양한 초밥 롤과 사시미.</p>
   </div>
   <div class="menu-item">
      <h3>버거</h3>
      <img src="data:image/jpeg;base64,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" width="200">
   </div>
</div>

<h2>Grid Layout Example:</h2>

<div class="grid-container">
   <div class="menu-item">
    	<h3>스테이크</h3>
    	<p>완벽하게 조리된 스테이크입니다.</p>
   </div>

	 	<div class="menu-item">  
	 		<h3>파스타</h3>
	 		<p>선택할 수 있는 소스와 함께 신선한 파스타입니다.</p>
	 	</div>

	 	<div class="menu-item">  
	 		<h3>초밥</h3>
	 		<p>다양한 초밥 롤과 사시미입니다.</p>
	 	</div>

	 	<div class="menu-item">  
	 		<h3>버거</h3>
         <a href="#">모든 재료가 들어간 맛있는 버거입니다.</a>
      </body>
</html>
