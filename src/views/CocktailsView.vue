<script>
    import axios from 'axios'
    import SingleCocktail from '../components/SingleCocktail.vue'
    export default {
    name: "CocktailsView",
    components: {
        SingleCocktail,
    },

    data() {
        return {
            cocktails: [],
        }
    },

    methods: {
        getCocktails(){
            axios.get('http://127.0.0.1:8000/api/cocktails', {
                params: {
                }
            })
            .then((response) => {
                console.log(response.data.results);
                this.cocktails = response.data.results;
            })
            .catch(function (error) {
                console.log(error);
            });  
        }
    },

    created() {
        this.getCocktails();
    },
    }
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h1 class="text-center py-3">Cocktails</h1>
            </div>
            <div class="col-4" v-for="cocktail in cocktails">
                <SingleCocktail :cocktail = 'cocktail'/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>