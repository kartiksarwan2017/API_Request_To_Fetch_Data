<!-- <script setup>
import axios from "axios";
// import { ref, onMounted  } from "vue";

// export default {

//     setup(){
//         const movies = ref([]);

//     const fetchMovies = async () => {

//         const options = {
//                 method: 'GET',
//                 headers: {
//                     accept: 'application/json',
//                     Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI4ZjcwOGZkMDlhNGFkZGM3MTczZDA3YzQ2ZGYyMDVlNCIsInN1YiI6IjY0NTkwMDI1NmFhOGUwMDExY2ExNDAzNiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.UXbpoC0_kBOKR8Npku7XpKdWH-ELp4k4qTWQUoyRVbk'
//                 }
//             };

//         try {
//             const { data: { results } } = await axios.get(`https://api.themoviedb.org/3/movie/popular`, options);
//             movies.value = results;
//             console.log(await axios.get(`https://api.themoviedb.org/3/movie/popular`, options));
//         }catch(error) {
//             console.log(error);
//         }
//     }

//     onMounted(() => {
//         fetchMovies();
//     })

//     return {
//         movies,
//     };
// }}

</script>

<template>
    <div>
        <h1>Breaking Bad Cards</h1>
        <div v-for="movie in movies" :key="movie.id">
            <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`" />
        </div>
    </div>
</template> -->




<script setup>
import axios from "axios";

    const options = {
        method: 'GET',
        headers: {
            accept: 'application/json',
            Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI4ZjcwOGZkMDlhNGFkZGM3MTczZDA3YzQ2ZGYyMDVlNCIsInN1YiI6IjY0NTkwMDI1NmFhOGUwMDExY2ExNDAzNiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.UXbpoC0_kBOKR8Npku7XpKdWH-ELp4k4qTWQUoyRVbk'
        }
    };
    const { data: { results } } = await axios.get(`https://api.themoviedb.org/3/movie/popular`, options);
    console.log(results);

</script>

<template>
    <div>
        <h1>Breaking Bad Cards</h1>
        <h1>{{ results }}</h1>
        <!-- <div v-for="movie in movies" :key="movie.id">
            <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`" />
        </div> -->
    </div>
</template>