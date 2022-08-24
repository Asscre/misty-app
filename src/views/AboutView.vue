<script setup lang="ts">
import { onMounted, ref } from 'vue';

function openDailog() {
  (window as any).MistyCallFlutter.postMessage('js call Flutter');
}

function getDataFormFlutter() {
  (window as any).MistyCallFlutter.postMessage('getDataFormFlutter');
}

const flutterData = ref('');
function flutterCallJs(param : any) {
  flutterData.value = param;
}

onMounted(() => {
  (window as any).flutterCallJs = flutterCallJs;
});
</script>

<template>
  <div class="about">
    <h2>这个页面用来展示Route</h2>
    <button @click="openDailog">打开弹窗</button>
    <button @click="getDataFormFlutter">获取Flutter数据并展示</button>
    <p>Flutter数据: {{ flutterData }}</p>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

.about {
  h2 {
    text-align: center;
  }

  button {
    display: block;
    margin: 20px auto;
    width: 100px;
    height: 30px;
    text-align: center;
    color: white;
    background-color: rgb(0, 149, 255);
    border: none;
    border-radius: 3px;
  }

  :nth-child(3) {
    width: 200px;
  }

  p {
    text-align: center;
    font-weight: 600;
    font-size: 20px;
  }
}

</style>
