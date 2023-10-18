<script>
    import Logo from "./logo.svelte";
    import Link from "./Link.svelte";
    import Lupa from "../assets/lupa.png";
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

<div class="flex-grow-1" ></div>

<button class="buttonclass"> SUSCRIBETE </button>
<button class="buttonsesion">Inciar sesión</button>

<img src={Lupa} alt="lupa" >


</header>
    

   <style>
       header {
        display:flex;
        justify-content: flex-start;
        align-items: center;
        margin: 20px 40px;
        gap: 20px;
       }

       .flex-grow-1 {
        flex-grow:1 !important;
       }
       
       .buttonclass {
        background-color:#02ffa1 ;
        border:none;
       }

       .buttonsesion{
        color:white;
        background-color: transparent;
        border:2px solid white;
       }
       
   </style>
