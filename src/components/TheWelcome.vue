<script setup lang="ts">
import WelcomeItem from "./WelcomeItem.vue";
import DocumentationIcon from "./icons/IconDocumentation.vue";
import ToolingIcon from "./icons/IconTooling.vue";
import EcosystemIcon from "./icons/IconEcosystem.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";
import JuejinIcon from "./icons/IconJuejin.vue";
import GithubIcon from "./icons/IconGithub.vue";
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>文档</template>
    Misty’s
    <a target="_blank" href="https://github.com/Asscre/misty-app">Github</a>
    让你的Flutter拥有小程序功能的功能体验.
    <br />
    Misty’s
    <a target="_blank" href="https://github.com/Asscre/misty-app">官方demo</a>
    帮助你快速了解如何集成属于你自己的Flutter小程序功能.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>项目规划</template>
    <br />
    ✅ Web 资源管理器 (版本管理，资源下载管理)
    <br />
    ✅ WebView 资源和网络代理
    <br />
    ☑️ Flutter 与 Web 项目原生交互
    <br />
    ☑️ Misty UI框架，帮助快速搭建 Misty 程序
    <br />
    更多详情了解请看 <code>README.md</code>.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>持续更新</template>

    保证每个自然月更新一版！😁
    <br /> 
    <br /> 
    为了保证正常版本更新和迭代，更新迭代的规则如下：
    <br />
    ⭕️  优先 版本开发 和 修复 BUG
    <br />
    ⭕️  然后是 需求榜
    <br />
    ⭕️  其次是 其他定制化
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>关注我</template>
    <JuejinIcon />
    <a href="https://juejin.cn/user/870468939942311">Asscre</a>
    <br />
    <GithubIcon />
    <a href="https://github.com/Asscre">Asscre</a>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>支持 Misty</template>

    <img class="logo"
      src="@/assets/WechatPay.jpeg"
      width="219"
      height="300">
  </WelcomeItem>
</template>
