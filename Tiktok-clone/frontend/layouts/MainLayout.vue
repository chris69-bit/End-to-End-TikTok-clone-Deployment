<template>
    <div>
        <TopNav/>
        <div 
          :class="route.fullPath === '/' ? 'max-w-[1140px]' : ''"
          class="flex justify-between w-full px-0 lg:px-2.5 mx-auto">
          <div>
            <SideNavMain/>

          </div>

        </div>

    </div>
</template>

<script setup>
const route = useRoute()
</script>




