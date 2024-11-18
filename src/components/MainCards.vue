<script setup>
import MainCardSingle from './MainCardSingle.vue';
import useAPI from '@/composables/useAPI';

const {employees} = useAPI()
</script>

<template>
    <!-- chosing grid, grid column 5, space between each picture 5, padding 10-->
<div class="grid grid-cols-5 gap-10 p-10">
   <MainCardSingle v-for="employee in employees" :key="employee._id" :employee="employee"></MainCardSingle> 
</div>

</template>