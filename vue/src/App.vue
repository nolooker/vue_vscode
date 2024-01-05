<template>

  <div class="black-bg" v-if="모달창열림 == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="모달창열림 = false">닫기</button>
    </div>
  </div>

  <!-- 상단 Nav 메뉴 -->
  <div class="menu">

    <a v-for="작명 in 메뉴들" :key="작명">{{ 작명 }}</a>

    <!-- <a>Home</a> -->
    <!-- <a>Products</a> -->
    <!-- <a>About</a> -->
  </div>

  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
<!--   
  <div v-for="h1 in products" :key="h1">{{ h1 }}
      <p v-for="가격 in price" :key="가격">{{ 가격 }}</p>
  </div> 
  
  <div v-for="(a,i) in products" :key="i">
    <h1>{{a}}</h1>
    <p>{{ price.price1 }} {{ won }}</p>  
  </div> -->

  <div>
    <h1 @click="모달창열림 = true">{{ products[0] }}</h1>
    <p>{{ price.price1 }} {{ won }}</p>
    <button @click=신고수[0]++>{{ complain }}</button> <span>신고수 : {{ 신고수[0] }}</span>
    <!-- {{ data 바인딩 }} -->
  </div>

  <div>
    <h1>{{ products[1] }}</h1>
    <p>{{ price.price2 }} {{ won }}</p>  
    <button @click=신고수[1]++>{{ complain }}</button> <span>신고수 : {{ 신고수[1] }}</span>
    <!-- {{ data 바인딩 }} -->
  </div>

  <div>
    <h1>{{ products[2] }}</h1>
    <p>{{ price.price3 }} {{ won }}</p>  
    <button @click=신고수[2]++>{{ complain }}</button> <span>신고수 : {{ 신고수[2] }}</span>
    <!-- {{ data 바인딩 }} -->
  </div>

</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      won : "만원",
      complain : "허위신고",

      모달창열림 : false,

      신고수 : [0,0,0],

      price : {
        price1 : 60,
        price2 : 100,
        price3 : "아무거나",
      },

      products : ['강남', '여의도', '강북'],
      메뉴들 : ['Home', 'Shop', 'About'],

      if(){

      }

    }
  },
  methods : {
    // vue에서 함수만들고 싶으면 methods:{} 안에 만든다.
    
    increase(){
      this.신고수 += 1;
    }
  },
  components: {
    
  }
}
</script>

<style>

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  background: black;
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 15px;
}

.menu a {
  color: white;
  padding: 10px;
}

</style>
