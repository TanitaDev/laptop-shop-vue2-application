<template>
     <div class="v-main-wrapper">
        <p>{{ title }}</p>
        <vCataloog></vCataloog>
        <vCart v-if="CART.length"></vCart>
     </div>
</template>

<script>
    import vCataloog from "./v-catalog";
    import vCart from "./v-cart";
    import { mapGetters } from "vuex";

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
        computed: {
            ...mapGetters([
                'CART'
            ])
        },
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