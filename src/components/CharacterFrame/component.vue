<template src="./template.html"></template>
<style src="./style.scss" lang="scss" scoped>
</style>

<script>
export default {
    props: {
        character: Object
    },
    computed: {
        link: function(){
            return `url(${this.character.imageURL})`
        }
    },
    methods: {
        emitName(){
            this.$emit("giveName", this.character)
        }
    }
};
</script>