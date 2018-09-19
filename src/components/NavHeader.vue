<template>
   <div>
       <header :id="$style.header">
             <!-- <img src="./assets/logo.png" alt="" srcset=""> -->
             <a href="" class="btn_download">下载App</a>
       </header>
        <nav class="navbar">
        <ul class="nav-list">
            <li class="nav-item" 
            v-for="(list) in navConfig" 
            :key="list.key">
            <router-link :to="list.href" tag="li" exact-active-class="active">{{list.name}}</router-link></li>
        </ul>
    </nav>
       </div> 
</template>
<script lang="ts" module>
import Vue from "vue";
import { constants } from 'http2';
import { throws } from 'assert';
export default Vue.extend({
  data():Object {
    return {
      navConfig: [
        {
          name: "推荐",
          key: 0,
          href: "/"
        },
        {
          name: "排行榜",
          key: 1,
          href: "/rank"
        },
        {
          name: "搜索",
          key: 2,
          href: "/search"
        }
      ]
    };
  },
  created(){
      console.log(this.$style);
  }
});
</script>
<style lang="scss" module>
// @import "./style/_var.scss";
  #header {
  display: flex;
  align-items: center;
  position: relative;
//   height: $header-height;
//   background: $header-background;
//   #logo {
//     height: $logo-height;
//     margin-left: 10px;
//   }
//   .btn_download {
//     position: absolute;
//     right: 10px;
//     height: 28px;
//     line-height: 28px;
//     font-size: 14px;
//     padding: 0 12px;
//     background: #149c5a;
//     color: #fff;
//     border-radius: 99px;
//   }
}
</style>


