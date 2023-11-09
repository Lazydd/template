<template>
    <VirtualList
        class="List"
        :height="500"
        :item-data="list"
        :item-count="list.length"
        :item-size="100"
        :item="Row"
        width="100%"
    />
</template>

<script setup lang="ts">
import { ref, markRaw } from "vue";
import Rows from "./Row.vue";
import VirtualList from "@tarojs/components/virtual-list";
const buildData = (offset = 0) => {
    return Array(100)
        .fill(0)
        .map((_, i) => i + offset);
};
const Row = markRaw(Rows);
const list = ref(buildData(0));
console.log(list.value);

</script>
