<template>
  <button @click="increaseValue">Add {{ value }}</button>
</template>

<script>
export default {
    data(){
        return {
            value: 10
        }
    },
    methods: {
        increaseValue(){
            this.$store.commit('increase', { value: this.value})
        }
    }
}
</script>

<style>

</style>