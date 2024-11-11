<script setup lang="ts">
import headerLogo from "./assets/header.svg";
import About1 from "./assets/About1.svg";
import About2 from "./assets/About2.svg";
import About3 from "./assets/About3.svg";
import About4 from "./assets/About4.svg";
import JLU from "./assets/吉林大学校徽.svg";
</script>

<template>
  <header>
    <img
      :src="headerLogo"
      style="width: 100%; height: 70%; pointer-events: none"
    />
    <div class="links">
      <a href="http://ans.museday.top" target="_blank">AAIR-Q&A</a>
      <a href="http://git.museday.top" target="_blank">AAIR-Gitea</a>
    </div>
  </header>
  <div class="about">
    <div
      style="
        font-size: 24pt;
        font-family: system-ui;
        font-weight: lighter;
        color: white;
      "
    >
      关于我们
    </div>
    <div class="about-items">
      <div class="about-item">
        <img :src="About1" style="width: 100px; height: 100px" />
        <div>跨学科</div>
        <div>提供交流平台，促进高新技术的多学科交叉应用</div>
      </div>

      <div class="about-item">
        <img :src="About2" style="width: 100px; height: 100px" />
        <div>竞赛</div>
        <div>为同学们参与各类竞赛提供组队和技术支持</div>
      </div>

      <div class="about-item">
        <img :src="About3" style="width: 100px; height: 100px" />
        <div>技术</div>
        <div>嵌入式、硬件、FPGA、机器人等方向的学习路线</div>
      </div>

      <div class="about-item">
        <img :src="About4" style="width: 100px; height: 100px" />
        <div>资源</div>
        <div>VR、3D打印、GPU服务器等诸多设备资源</div>
      </div>
      <div class="about-item spacer" style="width: 0%; height: 8em"></div>
    </div>
  </div>
  <footer>
    <div class="info">
      <div>社团活动地址：吉林大学李四光教学楼-501</div>
      <div>管理员信箱：lxl9923@mails.jlu.edu.cn</div>
      <a href="https://icp.gov.moe/?keyword=20240260" target="_blank"
        >萌ICP备20240260号</a
      >
    </div>
    <img :src="JLU" class="jlu" style="width: 4em; height: 4em" />
    <div class="link-exchange">
      <a href="https://vitejs.dev/guide/features.html" target="_blank"
        >吉林大学机器人梦工场</a
      >
    </div>
  </footer>
</template>

<style scoped>
.links {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 1rem;
}
header {
  place-content: center;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 91.6vh;
}
.links > a {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-weight: 100;
  color: #0c112a;
  /* text-decoration: none; */
}
.about {
  background-color: #0c112a;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 4em;
  /* flex-wrap: nowrap; */
  /* place-items: center; */
}
.about-items {
  display: grid;
  justify-content: center;
  width: 100%;
  gap: 6%;
  margin: 3em;
  grid-template-columns: repeat(auto-fit, minmax(12em, 1fr)); /* 新增代码 */
}
.about-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  /* width: 12em; */
}
.about-item > div {
  color: white;
  font-family: system-ui;
  font-weight: lighter;
  text-align: center;
}
.about-item > div:nth-child(1) {
  font-size: 36pt;
}
.about-item > div:nth-child(2) {
  font-size: 24pt;
}

footer {
  background-color: #010416;
  padding: 2em;
  display: flex;
  justify-content: space-between;
  place-items: center;
}
/* footer所有子元素 frow */
footer > * {
  width: 33.3vw;
}

footer > .info,
footer > .link-exchange {
  font-size: 9pt;
  color: white;
  font-family: system-ui;
  font-weight: lighter;
  display: flex;
  flex-direction: column;
  gap: 0.25em;
  height: 100%;
}
footer > * > a {
  color: white;
}

footer > .link-exchange {
  align-items: end;
}

@media (min-width: 600px) {
  .spacer {
    display: none;
  }
  .jlu {
    display: inline;
  }
}
@media (max-width: 600px) {
  .jlu {
    display: none;
  }
}
</style>
