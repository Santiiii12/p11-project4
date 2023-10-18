<script>
    import Logo from "./logo.svelte"
    import Link from "./Link.svelte";
</script>

<header>

<Logo />
 <nav>
       <Link text="Películas" />
       <Link text="Series" />
       <Link text="Colecciones" /> 
       <Link text="Festivales" />
       <Link text="Más"/>

</nav>

</header>
    

   <style>
       header {
        display:flex;
        justify-content: flex-start;
        align-items: center;
        margin: 20px 40px;
        gap: 20px;
       }
   </style>
