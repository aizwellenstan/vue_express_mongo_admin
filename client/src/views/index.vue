<template functional>
  <div class="bg">
    <div class="image-box__content">
      
    </div>
    <div class="red">
      Start bringing your vision to life today. Nadi's real-time 3D development platform empowers you with
      <br>
      all you need to create, operate, and monetize.
    </div>
    <div class="green">
      Nadi for all
    </div>
    <div class="yellow">
      <router-link to = "/ourproducts" ><button class="getstarted"><a>Get started</a></button></router-link>
      <router-link to = "/learn" ><button class="learnmore"><a>Learn more</a></button></router-link>
    </div>
    <div class="orange">
      <table class="blueTable">
        <tbody>
          <tr class="tr1">
            <td>
              <img style="margin-top: 17px;" src="../assets/img/account-icon-png-3.png" height="100px">
              <p style="margin-top: 5px; margin-bottom: 0px">Nadi ID</p>
            </td>
          </tr>
          <tr class="tr2">
            <td>
              A Nadi ID allows you to buy and/or subscribe to Nadi products and ser-
              <br>
              vices, shop in the Assert Store and participate in the Nadi community.
            </td>
          </tr>
          <tr class="tr3">
            <td>
              <router-link to = "/login"><button class="login"><a>Log in</a></button></router-link>
              <router-link to = "/register"><button class="create"><a>Create a NADI ID</a></button></router-link>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div> 
  
</template>


<style lang="scss" scoped>
  .bg {
    background-image: url('../assets/img/home_bg.png');
    height:100%;
    min-height: calc(100vh - 151px);
  }


  .red{
    position: fixed;
    z-index: 3;
    display: flex;
    height:60px;
    width:956px;
    // border: medium solid #e71919;
    margin-left:17.3%;
    margin-top:11%;
    color: lightblue;
    font: bold; 
    color: #fff;
    font-size: 1.8vh;
    line-height: 1.5
  }
  .green{
    position: fixed;
    z-index: 3;
    display: flex;
    height:90px;
    width:956px;
    // border: medium solid #23b665;
    margin-left:17.3%;
    margin-top:5%;
    color: #fff;
    font: bold; 
    font-size: 6.8vh
  }

  .yellow {
    position: fixed;
    z-index: 3;
    display: flex;
    height:1px;
    width:956px;
    // border: medium solid#d6ec10;
    margin-left:17.3%;
    margin-top: 13.8%;
    color: lightblue;
    font: bold; 
    font-size: 7.5vh
  }

  .getstarted {
    display: inline-block;
    padding: 10px 20px;
    border-radius: 3px;
    background: #32d4d7;
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 1.5vh;
    width: 150px;
  }

  .learnmore {
    display: inline-block;
    padding: 9px 20px;
    border: solid 2px #fff;
    border-radius: 3px;
    background: rgba(0,0,0,0.2);
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    font-family: Helvetica, Arial, sans-serif;
    height: 38px;
    font-size: 1.5vh;
    width: 150px;
    margin-left:13px
  }

  .orange {
    position: fixed;
    z-index: 3;
    display: flex;
    height:686px;
    width:600px;
    // border: medium solid#ec9410;
    margin-left:67%;
    margin-top:4.8%;
    color: lightblue;
    font: bold; 
  }

  table {
    width: 100%;
    color: black;
  }

  .tr1 {
    height: 200px;
    text-align: center;
    font-size: 4vh;
  }

  .tr2 {
    height: 82px;
    font-size: 1.6vh;
    text-align: center;
  }

  .tr3 {
    height: 43px;
    font-size: 2vh;
  }

  .login{
    margin-left: 110px;
    width: 149px;
    height: 100%;
    background-color: #32d4d7;
    color: #fff;
  }

  .create {
    margin-left: 5px;
    height: 100%;
    width: 220px;
    color: #32d4d7;
    border: medium solid#32d4d7;
  }
</style>
