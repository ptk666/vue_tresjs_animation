<template>
    <div class="px-5 pt-10 pb-0 md:px-16">
        <XyzTransitionGroup
            class="flex justify-between items-end overflow-hidden"
            appear
            xyz="down-100% duration-10 ease-in-out delay-2"
        >
            <div key="1" class="title font-bold text-xl">
                天
            </div>
            <ul key="2" class="flex gap-2">
                <li><a href="https://github.com/ptk666" target="_blank"><img src="/images/github.png" alt="github" width="20" height="20"></a></li>
                <li><a href="https://www.linkedin.com/in/brucejamesdelacruz/" target="_blank"><img src="/images/linkedin.png" alt="github" width="20" height="20"></a></li>
            </ul>
        </XyzTransitionGroup>
    </div>
</template>

<script setup>
</script>

<style>

</style>