<template>
    <div class="">
        <div v-for="photo in photos" v-bind:key="photo.id" class="is-6 columns is-vcentered">
            <figure class="image">
                <img v-bind:src="photo.urls.regular">
            </figure>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
let URL = "https://api.unsplash.com/search/photos?query=arabian&client_id=24f219760e48132fad4e804599f0212610efcba3bb53e4d9a9e15d8673053f7d"  

export default {
    data() {
        return {photos: []}
        },
    methods: {
        async getRandomPhoto () {
            const response = await axios.get(URL)
            this.photos = response.data.results;
        }
    },
    mounted(){
        this.getRandomPhoto();
    }
}
</script>