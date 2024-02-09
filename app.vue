<script lang="ts" setup>
const { data } = await useAsyncData("content", () => {
	return queryContent('/').findOne()
})
</script>

<template>
  <div>
		<ContentRenderer v-if="data" :value="data" />
  </div>
</template>
