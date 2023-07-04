<template>
  <div id ="wrap">
    <header>
      <a class="logo" href="App.vue">
        <img src="./assets/mainlogo.png" height="100px">
      </a>
      <nav>
        <ul class="nav-items">
          <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
        </ul>
      </nav>
    </header>
    <body>
      <span class="border-background"></span>
    </body>
  </div>
</template>

<script>

export default {
  name: 'App',
}
</script>

<style>
*{ 
  /* *전체 스타일에 적용하겠다. */
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

  .steprow>li{
    /* steplow에 있는 li만 아래 적용하겠다. */
    display: inline-block;
  }
  
  header{
    width: 100%;
    height: 100px;
    z-index: 2000; /*쌓임 순서*/
    background-color: #fff;
    box-shadow: 0 5px 2px rgba(0, 0, 0, 0.05), 0 1px 0 rgba(0, 0, 0, 0.05);
  }
  
  li{
    list-style: none;/*정렬 되지 않은 태그라서 앞에 점이 붙어서 없애주겠다.*/
  }
  
  a{
    text-decoration: none;/*a태그가 텍스트일 때 항상 밑줄이 붙어서 없애줘야함.*/
  }
  
  nav{
    float: right;
  }
  
  .logo{
    display:inline-block;/*inline-block 크기설정가능해짐*/
    height: 100px;
    margin: 12px 0 12px 50px;
  }
  
  .logo > img { height: 80px; }
  
  .nav-items > li {
    display: inline-block;
  }
  
  .nav-items > li > a {
    line-height: 100px;
    padding-right: 50px;
    color: rgba(0, 0, 0, 0.4);
    font-size:25px;
  }
  
  .nav-items > li > a:hover {/*a:ho*/
    color: rgba(0, 0, 0, 0.8);
  }

  .border-background{
    z-index: -1;
    border: 2px solid;
    position: absolute;
    bottom: 0;
    width: 90%;
    height: 75%;
    border-bottom: none;
    box-sizing: border-box;
    border-color: rgb(130, 130, 130);
    left: 50%;  /* 요소를 부모 요소의 중앙으로 이동시킵니다. */
    transform: translateX(-50%);
    padding: 120px 20px 0px 20px;
  }
  </style>