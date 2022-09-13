<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';

defineProps({
    posts: Array,
    title: String
});

</script>

<template>
<AppLayout title="Post">
    <template #header>
        <h2 class="font-semibold text-xl text-gray-800 leading-tight">
            Post
        </h2>
    </template>

    <div class="py-12">
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
            <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                <div v-for="post in posts" :key="post.id">
                    <p>{{post.name}} {{title}}</p>
                </div>
            </div>
        </div>
    </div>
</AppLayout>
</template>