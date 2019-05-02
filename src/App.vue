<template>
  <div id="app">
    <Header></Header>
    <section class="section1_bg">
      <main1></main1>
      <main2></main2>
    </section>
    <section class="section2_bg">
      <card></card>
    </section>
    <section class="section3_bg">
      <showing></showing>
    </section>
    <section class="section4_bg">
      <footer1></footer1>
    </section>
    <showcard :card="car" />

    <section class="section5_bg">
      
        <h1> Componente escolhido </h1>
        
        <button @click="compselect = 'Comp1'"> Componente 1 </button>
        <button @click="compselect = 'Comp2'"> Componente 2 </button>
        <button @click="compselect = 'Comp3'"> Componente 3 </button>
        <button @click="compselect = 'Assincrono'"> Assincrono </button>
        
        {{compselect}}
        <div class="appcomponbg">
        <component :is = "compselect"> </component>
        </div>
    
    </section>

  </div>
</template>

<script>

  import { Component, Vue } from 'vue-property-decorator'
  import Header from './components/header'
  import Main2 from './components/main2'
  import Main1 from './components/main1'
  import Card from './components/card'
  import Show from './components/showdiv3'
  import List from './components/list'
  import Footer from './components/footer'
  import ShowCard from './components/Showcard'
  import Comp1 from './components/Componente1'
  import Comp2 from './components/Componente2list'
  import Comp3 from './components/Componente3'

export default {

  components: {
    Assincrono: () => ({
        loading: { template: '<p> e agora </p>' },
        error: { template: '<p> Erro ao carregar component! </p>' },
        delay:200,
        timeout: 3000,
        component: new Promise((resolve,reject) =>{
          setTimeout(()=>{
            resolve(import('./components/Assincrono.vue'))
          },2000)
        }),
      }),
    'Header' : Header,
    'main2' : Main2,
    'main1' : Main1,
    'card' : Card,
    'showing' : Show,
    'list' : List,
    'footer1' : Footer,
    'showcard' : ShowCard,
    Comp1,
    Comp2,
    Comp3

  },
  data(){
    return{
    compselect : 'Comp1'
    }
  },
}

</script>

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
</style>
