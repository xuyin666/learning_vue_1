<template>
    <div class="school">
        <h2>School Name: {{name}}</h2>
        <h2>School Addresse : {{address}}</h2>
    </div>
</template>

<script>
    export default {
        name: 'School',
        data() {
            return {
                name: 'atGuigu',
                address: 'Pekin'
            }
        }
    }
</script>

<style>
    .school{
        background-color: gray;
    }
</style>