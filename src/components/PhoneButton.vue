<template>
    <div>
        <div class="rounded-full w-12 h-12 shadow-lg flex flex-col justify-center items-center font-sans cursor-pointer">
            <div class="text-md font-bold">{{ button.mainButton }}</div>
            <div class="text-xs font-normal">{{ button.subButton }}</div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['button']
};
</script>

<style></style>
