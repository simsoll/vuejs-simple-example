<template>
    <div>
        <button v-on:click="increment">
            {{ totalCount }}
        </button>
    </div>        
</template>

<script>
export default {
    props: {
        start: {
            type: Number,
            required: true
        }  
    },
    data: function() {
        return {
            counter: 0
        }
    },
    methods: {
        increment: function() {
            this.counter += 1
            this.$emit('increment')
        }
    },
    computed: {
        totalCount: function() {
            return this.start + this.counter;
        }
    }
}
</script>

<style lang="scss">

</style>
