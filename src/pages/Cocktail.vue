<script setup>
import { computed } from 'vue';
import { useRoute } from 'vue-router';
import AppLayout from "../components/AppLayout.vue";

const route = useRoute();
const cocktailId = computed(() => route.path.split('/').pop())
</script>

<template>
    <AppLayout imgUrl="/src/assets/img/bg-1.jpg">
        <div class="wrapper">
            <div v-if="!ingredient || !cocktails" class="info">
                <div class="title">Choose your drink</div>
                <div class="line"></div>
            </div>
        </div>
    </AppLayout>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'
</style>