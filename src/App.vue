<template>
<div>
  <div class="player">
    <div v-for="player in players" :key="player.id" class="player_style" @click="playerDetails(id)">
      {{player.pname}} id : {{player.id}}
    </div>
  </div>

  <div class="playerImage">
    <div v-for="(pi,index) in playerImage" :key="index">
      <img :src="pi" alt="">
    </div>
  </div>

  <div class="rawimg">
    <img src="./assets/img/pic1.jpg" alt="" class="cl big">
    <img src="./assets/img/pic2.jpg" alt="" class="cl medium">
    <img src="./assets/img/pic3.jpg" alt="" class="cl big">
    <img src="./assets/img/pic4.jpg" alt="" class="cl small">
    <img src="./assets/img/pic1.jpg" alt="" class="cl big">
    <img src="./assets/img/pic2.jpg" alt="" class="cl medium">
    <img src="./assets/img/pic3.jpg" alt="" class="cl big">
    <img src="./assets/img/pic4.jpg" alt="" class="cl small">
  </div>
</div>
</template>

<script>
export default {
  data(){
    return {
      players : [
        {pname: 'Shakib al hasan is the world most valuable player. He is our pride , we should proud to him',id: 1},
        {pname: 'Tamim was born in Chattogram. He is them most important player in our country',id: 2},
        {pname: 'Mashrafee is the great leader in our history of cricket. He is a true figher .',id: 3},
        {pname: 'mushfuq',id: 4},
        {pname: 'mahmudullah',id: 5},
        ],
        playerImage : [
        'https://source.unsplash.com/random/200x200?cat',
        'https://source.unsplash.com/random/200x200?rat',
        'https://source.unsplash.com/random/200x200?fish',
        'https://source.unsplash.com/random/200x200?girl',
        ],
      
    }
  },
  methods: {
    
  }
}
</script>

<style>
.player{
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}
.player_style{
  border: 1px solid black;
  padding: 20px;
  background: #ddd;
  margin: 10px;
}
.playerImage{
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
.cl{
  width: 200px;
  height: 300px;
  object-fit: cover;
}
.rawimg{
  display: flex;
  flex-wrap: wrap;
  margin: 15px;
}
.big{
  flex: 3;
}
.small{
  flex: 1;
  transition: all .3s ease-in;
}
.medium{
  flex: 2
}
.small:hover{
  scale: 2;
}
</style>