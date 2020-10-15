<template>
    <div>
        <h2>{{ info.data.results[0].name }}</h2>
        
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'CharacterItem',
    data () {
        return{
            info: null,
            loading: true,
            errored: false
        }
    },
    created () {
        
    },
    async mounted () {

        try {
            const idCharacter =  this.$route.params.id ;
            const {data} = await axios.get("https://gateway.marvel.com:443/v1/public/characters/"+idCharacter+"?apikey=55dd7a6256658f33a00034a161f9c8f7&ts=1&hash=8e821d4269b2d7f35e61d11ecd39ff92")
            this.info = data
        } catch (error) {
            this.errored = true;
        }
        this.loading = false;
    },
    methods: {

    }

}
</script>

<style>

</style>