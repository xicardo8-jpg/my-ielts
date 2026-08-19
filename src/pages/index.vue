<script setup lang="ts" generic="T extends any, O extends any">
import { RouterLink } from 'vue-router'

defineOptions({
  name: 'IndexPage',
})

const menus = reactive([
  {
    label: '词汇',
    icon: 'i-carbon-chart-histogram',
    link: '/vocabulary',
    desc: '雅思词汇真经与分场景词汇训练',
  },
  {
    label: '语法',
    icon: 'i-carbon-load-balancer-vpc ',
    link: '/grammar',
    desc: '针对雅思考试的语法课程与思维导图',
  },
  {
    label: '听力',
    icon: 'i-carbon-headphones',
    link: '/listening',
    desc: '179 考点词、听力技巧与精听训练',
  },
  {
    label: '口语',
    icon: 'i-carbon-microphone',
    link: '/speaking',
    desc: 'Part 1、Part 2、Part 3 个人素材整理',
  },
  {
    label: '阅读',
    icon: 'i-carbon-white-paper',
    link: '/reading',
    desc: '538 同义替换、定位词与错题复盘',
  },
  {
    label: '写作',
    icon: 'i-carbon-edit',
    link: '/writing',
    desc: 'Task 2 观点链、句型与作文修改',
  },
  {
    label: '单词练习',
    icon: 'i-carbon-keyboard',
    link: '/vocabulary/typing',
    desc: '跟打练习，提升单词读写熟悉度',
  },
])
</script>

<template>
  <div class="px-4 pt-6 2xl:px-0">
    <section class="mb-4 border border-gray-200 rounded-lg bg-white p-4 shadow-sm dark:border-gray-700 dark:bg-gray-800 sm:p-6">
      <div class="mx-auto max-w-screen-xl px-4 py-8 lg:px-6 sm:py-16">
        <h1 style="font-family: Charmonman;" class="mb-8 text-center text-5xl text-gray-900 dark:text-white sm:text-6xl">
          徐金 <span class="font-bold text-#f00">IELTS 7.0</span>
        </h1>
        <p class="mb-12 text-center text-lg text-gray-500 dark:text-gray-400">\n          从输入、输出到复盘，建立自己的雅思 7 分训练系统\n        </p>\n        <div class="mb-8 max-w-screen-md lg:mb-16">
          <h2 class="mb-4 text-4xl font-extrabold tracking-tight text-gray-900 dark:text-white">
            我的 IELTS 备考中心
          </h2>
          <p class="text-gray-500 sm:text-xl dark:text-gray-400">
            阅读重定位与逻辑，写作重论证与准确，口语重自然表达与展开。
          </p>
        </div>
        <div class="md:grid lg:grid-cols-3 md:grid-cols-2 md:gap-12 space-y-8 md:space-y-0">
          <RouterLink
            v-for="m in menus"
            :key="m.label"
            :to="m.link"
            class="block"
          >
            <div class="mb-4 h-10 w-10 flex items-center justify-center rounded-full bg-primary-100 lg:h-12 lg:w-12 dark:bg-primary-900">
              <i class="block h-5 w-5 text-primary-600 lg:h-6 lg:w-6 dark:text-primary-300" :class="m.icon" />
            </div>
            <h3 class="mb-2 text-xl font-bold dark:text-white">
              {{ m.label }}
            </h3>
            <p class="text-gray-500 dark:text-gray-400">
              {{ m.desc }}
            </p>
          </RouterLink>
        </div>
      </div>
    </section>
  </div>
</template>
