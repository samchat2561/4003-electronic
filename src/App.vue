<script setup>
import { RouterView } from 'vue-router';
import { computed, reactive } from 'vue';
import { useHead } from '@vueuse/head'
const siteData = reactive({
    title: 'สาขาวิชาช่างอิเล็กทรอนิกส์ วิทยาลัยเทคนิคตราด',
    description: 'สาขาวิชาช่างอิเล็กทรอนิกส์ วิทยาลัยเทคนิคตราด อาชีวศึกษา'
})

useHead({
    title: computed(() => siteData.title),
    meta: [
        {
            name: 'description',
            content: computed(() => siteData.description)
        }
    ]
})

</script>

<template>
 
  <router-view />
</template>

<style lang="scss" scoped>

</style>