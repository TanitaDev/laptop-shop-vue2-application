<template>
     <div class="v-main-wrapper">
        <p>{{ title }}</p>
        <vCataloog></vCataloog>
        <vCart></vCart>
     </div>
</template>

<script>
    import vCataloog from "./v-catalog";
    import vCart from "./v-cart";

    export default {
        name: "v-main-wrapper",
        components: {
            vCataloog,
            vCart
        },
        props: {},
        data() {
            return {}
        },
        computed: {},
        methods: {},
        watch: {},
        mounted: {
        },
    }
</script>

<style lang="sass">
    .v-main-wrapper
        max-width: 900px
        margin: 0 auto
</style>