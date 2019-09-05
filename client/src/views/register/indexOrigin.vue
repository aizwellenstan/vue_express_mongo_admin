<template>
  <div>
    <div class="navbar">
      <router-link to="/">
        <img src="../../assets/img/img_logo_nadi_1.png" class="logo">
      </router-link>
    </div>
    <div class="form">
      <span class="title">Create a NADI ID</span>
      <br>
      <br>
      If you already have a NADI ID, please <router-link to="/login" class="lightblue">sign in here</router-link>.
      <br>
      <br>
      <div class="filter-container" hight="calc(100%-72px)">
        <div class="filter-item el-input el-input--medium" style="width: 571px;">
          <span class="tag">Username</span><br>
          <input v-model="model.username" type="text" autocomplete="off" class="el-input__inner">
        </div>
        <div class="filter-item el-input el-input--medium" style="width: 571px; padding-left:28px">
          <span class="tag">Email</span><br>
          <input v-model="model.email" type="text" autocomplete="off" class="el-input__inner">
        </div>
      </div>

      <div class="filter-container" style="padding-top: 40px">
        <div class="filter-item el-input el-input--medium" style="width: 571px;">
          <span class="tag">Password</span><br>
          <input v-model="model.password" type="text" autocomplete="off" class="el-input__inner">
        </div>
        <div class="filter-item el-input el-input--medium" style="width: 571px; padding-left:28px">
          <span class="tag">Confirm Password</span><br>
          <input v-model="model.comfirmPassword" type="text" autocomplete="off" class="el-input__inner">
        </div>
      </div>
      <div class="filter-container" style="padding-top: 40px">
        <div class="filter-item el-input el-input--medium" style="width: 571px;">
          <span class="tag">Fullname</span><br>
          <input type="text" autocomplete="off" class="el-input__inner">
        </div>
      </div>
      <br>
      <input type="checkbox"> I agree to the NADI
      <router-link to="/termsofuse" class="lightblue">Terms of Use</router-link> and
      <router-link to="/privacy" class="lightblue">Privacy Policy</router-link>
      <br>
      <input type="checkbox">
      I understand that by checking this box, I am agreeing to recive<br>
      &nbsp;&nbsp;&nbsp;&nbsp;promotional materials from NADI
      <div style="padding-top: 21px">
        <a><button class="btn-cyan" @click='post'>Create a Nadi ID</button></a>
        <router-link to="/login">
          <button class="btn-white" type="submit">Already have a Nadi ID?</button>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import Methods from '@/api/methods'

export default {
  name: 'HelloWorld',
  data() {
    return {
      model: {}
    }
  },
  methods: {
    async post() {
      const element = { model: this.model }
      const response = await Methods.registerPosting(element)
      console.log(response.data.message)
    }
  }
}
</script>

<style lang="scss" scoped>
.logo {
  width: 63px;
  height: 32px;
  margin-left: 76px;
  margin-top: 20px;
}
.navbar {
  height: 72px;
  overflow: hidden;
  position: relative;
  position: fixed; /* Set the navbar to fixed position */
  top: 0; /* Position the navbar at the top of the page */
  width: 100%;
  background: #fff;
  box-shadow: 0 1px 4px rgba(0,21,41,.08);
  z-index: 1001;
  .hamburger-container {
    line-height: 46px;
    height: 100%;
    float: left;
    cursor: pointer;
    transition: background .3s;
    -webkit-tap-highlight-color:transparent;
    &:hover {
      background: rgba(0, 0, 0, .025)
    }
  }
  .breadcrumb-container {
    float: left;
  }
  .errLog-container {
    display: inline-block;
    vertical-align: top;
  }
  .right-menu {
    float: right;
    height: 100%;
    line-height: 50px;
    &:focus {
      outline: none;
    }
    .right-menu-item {
      display: inline-block;
      padding: 0 8px;
      height: 100%;
      font-size: 18px;
      color: #5a5e66;
      vertical-align: text-bottom;
      &.hover-effect {
        cursor: pointer;
        transition: background .3s;
        &:hover {
          background: rgba(0, 0, 0, .025)
        }
      }
    }
    .avatar-container {
      margin-right: 30px;
      .avatar-wrapper {
        margin-top: 5px;
        position: relative;
        .user-avatar {
          cursor: pointer;
          width: 40px;
          height: 40px;
          border-radius: 10px;
        }
        .el-icon-caret-bottom {
          cursor: pointer;
          position: absolute;
          right: -20px;
          top: 25px;
          font-size: 12px;
        }
      }
    }
  }
}
.form {
  margin-top:72px;
  padding-top:68px;
  padding-left:377px;
  padding-bottom: 0;
  height: calc(100%-72px)
}
.lightblue {
  color: #32d4d7
}
.tag {
  font-size: 16px;
  color: #666
}
.title {
  font-size: 28px
}
.btn-cyan {
  background-color: #32d4d7;
  color: #fff;
  width: 176px;
  height: 40px
}
.btn-white {
  background-color: #fff;
  color: #32d4d7;
  width: 223px;
  height: 40px
}
</style>
