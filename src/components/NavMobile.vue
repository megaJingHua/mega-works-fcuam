<template>
  <div class="hidden-md-and-up">
    <el-button class="nav-mobile" @click="drawer = true" circle type="info">
      <i class="el-icon-s-unfold"></i>
    </el-button>
    <el-button class="nav-mobile-back" @click="back" circle size="mini" round>
      <i class="el-icon-back"></i>
    </el-button>
    <el-drawer :visible.sync="drawer" size="80%" :with-header="false" >
      <div class="pa-3" style="height: 100vh; overflow: auto">
        <div @click="changePage('/')">
          <el-image
            style="width: 100%; padding: 0px 2px"
            :src="require('@/assets/logo.png')"
          ></el-image>
        </div>
        <el-menu
          default-active="2"
          class="el-menu-vertical-demo"
        >
          <el-menu-item index="1"
            ><div @click="changePage('/news')">+ 最新消息</div></el-menu-item
          >
          <el-menu-item index="2"
            ><div @click="changePage('/recruit')">+ 招生資訊</div></el-menu-item
          >
          <el-submenu index="3">
            <template slot="title">+ 關於本系</template>
            <el-menu-item index="3-1"
              ><div @click="changePage('/history')">系史</div></el-menu-item
            >
            <el-menu-item index="3-2"
              ><div @click="changePage('/characteristic')">特色</div></el-menu-item
            >
            <el-menu-item index="3-3"
              ><div @click="changePage('/goal')">教育目標</div></el-menu-item
            >
            <el-menu-item index="3-4"
              ><div @click="changePage('/capability')">核心能力</div></el-menu-item
            >
            <el-menu-item index="3-5"
              ><div @click="changePage('/scholarship')">獎學金</div></el-menu-item
            >
            <el-menu-item index="3-6"
              ><div @click="changePage('/highlight')">本系亮點</div></el-menu-item
            >
          </el-submenu>
          <el-submenu index="4">
            <template slot="title">+ 課程規劃</template>
            <el-menu-item index="4-1"
              ><div @click="changePage('/course')">課程列表</div></el-menu-item
            >
            <el-menu-item index="4-2"
              ><div @click="changePage('/program')">學分學程</div></el-menu-item
            >
            <el-menu-item index="4-3"
              ><div @click="changePage('/innovation')">創新學制</div></el-menu-item
            >
          </el-submenu>
          <el-menu-item index="5"
            ><div @click="changePage('/teacher')">+ 師資介紹</div></el-menu-item
          >
          <el-submenu index="6">
            <template slot="title">+ 學生專區</template>
            <el-menu-item index="6-1"
              ><a href="https://myfcu.fcu.edu.tw/main/infomyfculogin.aspx" target="_blank"
                >逢甲人資訊服務入口</a
              ></el-menu-item
            >
            <el-menu-item index="6-2"
              ><a href="https://gomail.fcu.edu.tw/" target="_blank"
                >校園信箱</a
              ></el-menu-item
            >
            <el-menu-item index="6-3"
              ><a href="http://learningportfolio.fcu.edu.tw/tw/index.aspx" target="_blank"
                >Learning Portfoilo</a
              ></el-menu-item
            >
            <el-menu-item index="6-4"
              ><a href="https://coursesearch03.fcu.edu.tw/main.aspx" target="_blank"
                >逢甲大學課程檢索系統</a
              ></el-menu-item
            >
          </el-submenu>
          <el-submenu index="7">
            <template slot="title">+ 微積分資源</template>
            <el-menu-item index="7-1"
              ><a href="https://sway.office.com/JuWlSNVfTcAbs7aS?ref=Link" target="_blank"
                >微積分教學中心</a
              ></el-menu-item
            >
            <el-menu-item index="7-2"
              ><a
                href="http://140.134.140.30/~t97066/?ctNode=38709&idPath=5000_38705_38709"
                target="_blank"
                >主題式動畫影音教學</a
              ></el-menu-item
            >
            <el-menu-item index="7-3"
              ><a
                href="http://140.134.140.84/teachingcalculus/?ctNode=38712&idPath=5000_38705_38712"
                target="_blank"
                >工科微積分網路教學</a
              ></el-menu-item
            >
            <el-menu-item index="7-4"
              ><a
                href="https://www.junyiacademy.org/many-great-teachers/feng-chia-calculus"
                target="_blank"
                >商科微積分網路教學</a
              ></el-menu-item
            >
            <el-menu-item index="7-5"
              ><a
                href="http://140.134.140.60/calculus-ggb/?ctNode=40542&idPath=5000_38705_40542"
                target="_blank"
                >微積分動態教具</a
              ></el-menu-item
            >
            <el-menu-item index="7-6"
              ><a href="https://sites.google.com/site/calculusteaching/" target="_blank"
                >微積總棟員</a
              ></el-menu-item
            >
          </el-submenu>
        </el-menu>
      </div>
    </el-drawer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      drawer: false,
    };
  },
  methods: {
    changePage(router) {
      window.scrollTo(0, 0);
      this.drawer = false;
      if (this.$route.path !== router) {
        this.$router.push({ path: router });
      }
    },
    back() {
      this.$router.go(-1);
    },
  },
};
</script>
<style scoped>
.nav-mobile-back {
  position: fixed;
  top: 14px;
  left: 5px;
  z-index: 999;
}
.nav-mobile {
  position: fixed;
  top: 12px;
  right: 14px;
  z-index: 999;
}
</style>
