<script setup>
    definePageMeta({
        layout: "custom"
    });

    const router = useRoute();
    const { toTitleCase } = useTitleCase();

    useHead({
        title: `${router.params.make ? toTitleCase(router.params.make) : 'Cars'} in ${toTitleCase(router.params.city)}`
    });

</script>

<template>
    <div class="mt-20 flex">
        <CarSideBar />
        <NuxtPage/>
    </div>
</template>

