<template>
  <div class="hello">
    <img src="../assets/huawei.png" alt="" class="logo">
    <div class="tip">点击上方桌面按钮进入</div>
    <img src="../assets/uu.png" alt="" class="tipImg tip1">
    <img src="../assets/uu.png" alt="" class="tipImg tip2">
    <div class="wrap">
      <div class="item firstItem" :style="type==='all'?'margin-right:5%':''" v-if="type!=='person'">
        <img src="../assets/edu.png" alt="" class="itemImg firstImg">
        <div class="itemFont">
          <div class="bigFont">教学桌面</div>
          <div class="smallFont">Teaching Desktop</div>
        </div>
      </div>
      <div class="item secondItem" v-if="type!=='teacher'">
        <img src="../assets/ind1.png" alt="" class="itemImg secImg">
        <div class="itemFont">
          <div class="bigFont">个人桌面</div>
          <div class="smallFont">Personal Desktop</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        type: 'all'
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello {
    /* display: flex;
    justify-content: center;
    align-items: center; */
    height: 100%;
    width: 100%;
  background: #296683;

  }

  .wrap {
    /* display: flex;
    justify-content: center; */
    width: 50%;
    height: 200px;
    /* border: 1px solid gainsboro; */
    padding: 20px;
    box-sizing: border-box;
    position: absolute;
    top:0;
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
  }

  .secondItem {
    /* display: flex;
    justify-content: space-between;
    align-items: center;
    flex: 0 0 45%; */
    width:45%;
    height: 100%;
    display:inline-block;
    background: #74bfaf;
    box-sizing: border-box;
    padding: 0 60px;
    border-radius: 20px;
    cursor: pointer;
    transition: all linear .3s;
    box-shadow: 0px 0px 10px grey;

  }

  .firstItem {
    background: #da378d;
    /* display: flex;
    justify-content: space-between;
    align-items: center;
    flex: 0 0 45%; */
    width:45%;
    height: 100%;
    display:inline-block;
    box-sizing: border-box;
    padding: 0 60px;
    border-radius: 20px;
    cursor: pointer;
    transition: all linear .3s;
    box-shadow: 0px 0px 10px grey;

  }

  .item:hover {
    box-shadow: 2px 5px 15px grey;
  }

  .itemImg {
    height: 100px;
    width: 100px;
  }

  .firstImg {
    border-radius: 10px;
    box-shadow: 0px 0px 5px white;
    transition: all linear .2s;
    margin-top: 30px;
    margin-right: 30px;

  }

  .secImg {
    border-radius: 10px;
    box-shadow: 0px 0px 5px white;
    margin-top: 30px;
    margin-right: 30px;

  }

  .item:hover .firstImg,
  .item:hover .secImg {
    box-shadow: 0px 0px 10px white;

  }

  .itemFont {
    color: white;
    float: right;
    margin-top: 35px;
    /* display: inline-block; */
  }

  .bigFont {
    font-size: 30px;
    margin-bottom: 20px;
    transition: all linear .2s;
  }

  .smallFont {
    font-size: 20px;
    transition: all linear .2s;
  }

  .item:hover .bigFont,
  .item:hover .smallFont {
    text-shadow: 0px 0px 2px white;

  }

  .logo {
    position: absolute;
    top: 5%;
    left: 2%;
  }

  .tip {
    position: absolute;
    left: 0;
    right: 0;
    top: 67%;
    margin: 0 auto;
    font-size: 22px;
    color: white;

  }

  .tipImg {
    position: absolute;
    left: 0;
    right: 0;
    top: 59%;
    margin: 0 auto;
    font-size: 24px;
    color: white;
    width: 60px;
  }

  .tip1 {
    animation: ss infinite 1.5s ease-in-out;
  }

  .tip2 {
    top: 60.6%;
    animation: ss infinite 1.5s ease-in-out;

    /* animation-delay: .2s; */
  }

  @keyframes ss {
    0% {
      transform: scale(1)
    }

    50% {
      transform: scale(1.1)
    }

    100% {
      transform: scale(1)
    }
  }

</style>
