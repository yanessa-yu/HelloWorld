<template>
  <div class="hello">
    <div id="task4">
      <img src="../assets/scape.png" alt="">
    </div>
    <div id="task5">
     
    </div>
  </div>
</template>

<script>
// git地址   https://github.com/yushuanggui/HelloWord
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {}
  },
  methods: {
    sendRequest(){
      const xhr = new XMLHttpRequest()
      xhr.open('GET', "/test.json")
      xhr.onload = function(res){
        console.log(res)
      }
      xhr.send()

    }
  },
  mounted(){
    this.sendRequest()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#task4{
  position: fixed;
  width: 400px;
  height: 264px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;

  animation-duration: 1s;
  animation-name: task4;
  animation-iteration-count: infinite;
}
#task4 img{width: 400px;}
@keyframes task4 {
  from {
    transform: rotate(0deg); 
  }

  to {
    transform: rotate(90deg);
  }
}
@media screen and (max-width: 640px) {
  #task5{
    background-image: url(../assets/moblie.png);
    background-size: 100%;
    height: 3400px;
  }
}
@media screen and (min-width: 640px) and (max-width: 980px) {
  #task5{
    background-image: url(../assets/ipad.jpg);
       background-size: 100%;
    height: 3400px;
  }
}
@media screen and (min-width: 980px) and (max-width: 1920px) {
  #task5{
    background-image: url(../assets/PC.jpg);
    background-size: 100%;
    height: 3400px;
  }
}
</style>
