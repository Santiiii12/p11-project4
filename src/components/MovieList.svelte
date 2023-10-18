<script>
    import { onMount } from "svelte";

    const url = 'https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=es-US&page=1&sort_by=popularity.desc'
    const options = {
       method: 'GET',
       headers: {
    accept: 'application/json',
    Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI5YmQwMjc1NGUzZWFiMzljMDQzZmU3ZmI5NTY2N2QzMyIsInN1YiI6IjY1MmY4NWE5ZWE4NGM3MDEwYzFkZmYxNSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.8pnPkKuzkh0AHZAtIxS0gFWYP8aDc7zrz-FcekkqWlo'
  }
};

let movies = [];

onMount( () => fetch (url, options)
  .then(response => response.json())
  .then( data => movies = data.results)
  .catch(err => console.error(err)));

</script>
<div>
{ #each movies as movie }
       <img alt="Cover" src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}>
{/each}

</div>

<style>
    div {
        display: flex;
        flex-wrap:wrap;
        justify-content: center;
        gap: 15px;
    }

    img {
     height :121px;
     width:215px;
     object-fit: cover;

    }
</style>