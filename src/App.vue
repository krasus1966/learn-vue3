<template>
  <!--  <img alt="Vue logo" src="./assets/logo.png">-->
  <!--  <h1>{{ count }}</h1>-->
  <!--  <h1>{{ double }}</h1>-->
  <!--  <button @click="increate">+1</button>-->
  <div class="container">
    <global-header :user="currentUser" ></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import {ref, computed, defineComponent} from 'vue';
import 'bootstrap/dist/css/bootstrap.min.css'
import GlobalHeader, {UserProps} from "@/components/GlobalHeader.vue";
import ColumnList, {ColumnProps} from "@/components/ColumnList.vue";

const currentUser: UserProps = {
  isLogin: true,
  name: 'Krasus1966',
  id: 123,
}
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee'
  },
  {
    id: 2,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee'
  },
  {
    id: 3,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee'
  },
  {
    id: 4,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: '../assets/logo.png'
  },
  {
    id: 5,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee'
  },
  {
    id: 6,
    title: 'test1的专栏',
    description: 'xxxxxxxxxxxxxxxxxxxxx',
    avatar: 'http://vue-maker.oss-cn-hangzhou.aliyuncs.com/vue-marker/5ee'
  },
]
export default defineComponent({
  name: 'App',
  components: {
    ColumnList,
    GlobalHeader,
  },
  setup() {
    return {
      list: testData,
      currentUser: currentUser
    }
  }
})
// export default {
//   name: 'App',
//   setup() {
//     const count = ref(0)
//     const double = computed(() => {
//       return count.value * 2
//     })
//     const increate = () => {
//       count.value++
//     }
//     return {
//       count,
//       double,
//       increate
//     }
//   }
// };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
