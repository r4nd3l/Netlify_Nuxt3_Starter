<template>
  <div class="grid grid-col-12">
    <div class="col-span-12">
      <div class="flex flex-row justify-start items-center border border-red-500">
        <ul class="flex flex-row justify-start items-center gap-4 shadow w-full p-4">
          <li v-for="(item, index) in navigationTree" :key="index">
            <NuxtLink :to="item._path === '/main' ? '/' : item._path">
              {{ item.title }}
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  navigationTree: {
    type: Array,
    default: () => [],
  },
});
</script>

<style lang="scss" scoped>
div {
  content: "";
}
</style>
