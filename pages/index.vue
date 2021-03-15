<template>
  <div class="container mx-auto">
    <div class="bg-gray-900 shadow overflow-hidden sm:rounded-lg my-4">
      <div class="px-4 py-5 sm:px-6">
        <h3 class="text-md leading-6 font-medium text-gray-500">
          機能紹介
        </h3>
      </div>
      <div class="border-t border-gray-700">
        <dl class="divide-y divide-gray-800">
          <div class="bg-gray-900 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
            <dt class="text-sm font-medium text-gray-400">
              絵巻欠片
            </dt>
            <dd class="mt-1 text-sm text-gray-500 sm:mt-0 sm:col-span-2">
              絵巻イベント用計算機。欠片獲得状況の計算と記録ができます。
            </dd>
          </div>
          <div class="bg-gray-900 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
            <dt class="text-sm font-medium text-gray-400">
              火力計算
            </dt>
            <dd class="mt-1 text-sm text-gray-500 sm:mt-0 sm:col-span-2">
              式神の火力計算機です。
            </dd>
          </div>
          <div class="bg-gray-900 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
            <dt class="text-sm font-medium text-gray-400">
              百戦管理
            </dt>
            <dd class="mt-1 text-sm text-gray-500 sm:mt-0 sm:col-span-2">
              異聞ダンジョン百戦アタックモードの攻略管理ツールです。
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
    }
  }
}
</script>
