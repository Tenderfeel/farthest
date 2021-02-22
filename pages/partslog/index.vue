<template>
  <main class="main">
    <h1 class="page-title hidden">絵巻欠片計算機</h1>

    <div class="container mx-auto grid sm:grid-cols-2 gap-4 mt-4">
      <!-- 左 -->
      <div class="shadow overflow-hidden sm:rounded-md order-2 sm:order-1">
        <div class="bg-gray-900 px-3 py-3 sm:p-4">
          <div class="grid grid-cols-6 gap-6">
            <div class="col-span-2">
              <label for="small" class="label">欠片・小</label>
              <input
                type="number"
                name="small"
                id="small"
                min="0"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md"
              />
            </div>

            <div class="col-span-2">
              <label for="medium" class="label">欠片・中</label>
              <input
                type="number"
                name="medium"
                id="medium"
                min="0"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md"
              />
            </div>

            <div class="col-span-2">
              <label for="large" class="label">欠片・大</label>
              <input
                type="number"
                name="large"
                id="large"
                min="0"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md"
              />
            </div>
          </div>
        </div>
        <div class="p-3 bg-gray-900 text-center">
          <button type="button" name="button" class="btn btn-danger">
            リセット
          </button>
          <button type="button" class="btn btn-primary">
            ログ保存
          </button>
        </div>
      </div>
      <!-- 右 -->
      <div class="bg-gray-900 shadow overflow-hidden sm:rounded-md order-1 sm:order-2">
        <h2 class="leading-6 font-medium text-gray-500 p-2">合計ポイント</h2>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: 'PartsLogIndex',
  head() {
    return {
      title: '絵巻欠片計算機'
    }
  }
}
</script>
