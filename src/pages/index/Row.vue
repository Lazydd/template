<template>
    <view :id="id" :class="index % 2 ? 'ListItemOdd' : 'ListItemEven'">
        Row {{ index }} : {{ data[index] }}
    </view>
</template>

<script setup lang="ts">
defineProps<{
    id: any;
    index: any;
    data: any;
    isScrolling: any;
}>();
</script>
