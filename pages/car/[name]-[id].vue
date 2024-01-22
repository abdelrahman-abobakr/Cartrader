<script setup>
    definePageMeta({
        layout:"custom"
    });

    const route = useRoute();
    const { toTitleCase } = useTitleCase();
    useHead({
        title: toTitleCase(route.params.name) 
    });
</script>

<template>

    <CarDetailsHero/>

    <CarDetailsAttributes>Leather Interior</CarDetailsAttributes> 
    <CarDetailsAttributes>Wide Area</CarDetailsAttributes> 

    <CarDetailsDescription>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Exercitationem
        consequuntur, et saepe sequi, ipsum quisquam iste autem quas vel aperiam
        laboriosam dolorum vero tempore placeat, asperiores alias magni. Nulla,
        dolores.
    </CarDetailsDescription>
    
    <CarDetailsContact/>

</template>