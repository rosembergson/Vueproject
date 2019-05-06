<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  width:100%vw;
  height:100%hw;
}

.section1_bg{
  margin-top:-40px;
  display:flex;
  justify-content: space-around;
  margin-bottom:0;
}

.section2_bg{
  margin:130px 0;
  display:flex;
  justify-content: space-around;
  margin-bottom:0;
}

.section3_bg{
  margin:100px 0;
  display:flex;
}

.section4_bg{
  
}
.appcomponbg{
  width:100%;
  height:500px;
}
showcard{
  width:100%;
}
.section6_bg{
  width:100%;
}
</style>
