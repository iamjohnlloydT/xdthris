<script setup>
import sidebar from "@/Components/Sidebar.vue";
</script>

<template>
    <!--Header-->
    <div>
        <slot name="title"></slot>
    </div>

    <div class="grid max-w-full grid-cols-12">
        <!--Side Bar-->
        <div class="col-span-2 border-gray-300 sm:col-span-2">
            <sidebar />
        </div>

        <!--Main Content-->
        <div class="col-span-10 bg-[#F0F0F0] sm:col-span-10 block">
            <slot name="body"></slot>
        </div>
    </div>
    <Footer />
</template>
