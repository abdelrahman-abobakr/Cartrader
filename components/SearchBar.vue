<script setup>
    const city = ref("");
    const cityError = ref(false);

    const handleSearch = () =>{

        if (!city.value){
            return cityError.value = true;
        }
        navigateTo(`/city/${city.value}/car`);
    };
</script>

<template>
    <div
        class="font-serif  w-[600px] h-[45px] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto"
    >
        <input
        type="text"
        class="py-3 px-5 w-full text-lg rounded-full focus:outline-none"
        placeholder="Search by city..."
        v-model="city"
        :class="cityError? 'border border-red-500':''"
        />
        <button @click="handleSearch" class="bg-sky-500 px-10 text-white" >Search</button>
    </div>
</template>