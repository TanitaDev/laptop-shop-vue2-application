<template>
    <div class="v-catalog-item">
        <img :src=" require('../assets/images/' + product_data.image) " alt="">
        <p class="v-catalog-item__name">{{ product_data.name }}</p>
        <p class="v-catalog-item__price">Price: {{ product_data.price }}</p>
        <button 
            class="v-catalog-item__add_to_cart_btn btn" 
            @click="addToCart">Add to cart</button>
    </div>
</template>

<script>
   export default {
       name: "v-catalog-item",
       components: {},
       props: {
        product_data: {
            type: Object,
            default() {
                return {}
            }
        }
       },
       data() {
           return {}
       },
       computed: {},
       methods: {
        addToCart(){
            this.$emit("addToCart", this.product_data)
        }
       },
       watch: {},
       mounted: {
       },
   }
</script>

<style lang="sass">
    $padding: 8px
    $margin: 8px
    $radius: 4px

    .v-catalog-item
        flex-basis: 25%
        box-shadow: 0 0 8px #e0e0e0
        padding: $padding*2
        margin-bottom: $margin*2
</style>