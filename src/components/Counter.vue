<template>
    <div class="counter">
        <button class="plus" @click="plus">+</button>
        <span class="value">{{value}}</span>
        <button class="minus" @click="minus">-</button>
    </div>
</template>

<script>
    export default {
        name: 'counter',
        props: {
            index: Number,
            value: Number,
        },
        methods: {
            minus: function () {
                this.$emit('update', this.index, this.value - 1)
            },
            plus: function () {
                this.$emit('update', this.index, this.value + 1)
            }
        }
    }
</script>
<style scoped>

</style>
