<script>

</script>

<template>
    <div class="flex-1 px-3 py-4 space-y-2 overflow-y-auto">
        <RouterLink
        v-for="item in menuItems"
        :key="item.title"
        :to="item.route"
        class="flex items-center gap-3 p-3 rounded-xl transition-all duration-200 hover:bg-indigo-600 hover:text-white group"
        >
        <component :is="item.icon" class="w-6 h-6 shrink-0" />
        <span
            v-if="!isCollapsed"
            class="font-medium whitespace-nowrap transition-opacity duration-200">
            {{ item.title }}
        </span>

        <div
            v-if="isCollapsed"
            class="fixed left-20 ml-2 px-2 py-1 bg-indigo-600 text-white text-sm rounded opcaity0 group-hover:opacity-100 poim">

        </div>
        </RouterLink>
    </div>
</template>

<style>

</style>