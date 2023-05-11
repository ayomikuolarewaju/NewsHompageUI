<script> 
import img8 from '../img/logo.svg'; 
import img2 from '../img/icon-menu.svg';
import img1 from '../img/icon-menu-close.svg';
let rev = true;
const reveler = ()=>{
    rev = !rev;
}
</script>



<div class="container flex flex-row mx-auto justify-between mb-2 relative overflow-hidden">
    <div >
        <img src="{img8}" alt="" srcset="">
    </div>
    <div class="space-x-5 hidden md:flex md:flex-row">
        <a href="/">Home</a>
        <a href="/">New</a>
        <a href="/">Popular</a>
        <a href="/">Trending</a>
        <a href="/">Categories</a>
    </div>
    <div class="md:hidden cursor-pointer" on:click={reveler} on:keydown>
        <img src="{img2}" alt="" srcset="" >
    </div>
</div>

    
{#if rev}
<div class="container flex flex-row mx-auto justify-between mb-2 absolute bg-white
 z-50 w-2/3 h-full left-40 md:hidden overflow-hidden">
    <div class="absolute left-10 bg-white z-50  w-2/3 h-full">
        <div class="bg-white z-50 cursor-pointer  w-2/3 h-full absolute -right-32" on:click={reveler} on:keydown>
            <img src="{img1}" alt="" srcset="" class="md:hidden text-right">
        </div>
        <div class="space-x-5 md:hidden flex flex-col absolute top-40 left-10 text-2xl bg-white z-50 w-2/3 h-full">
            <a href="/" class="ml-5">Home</a>
            <a href="/">New</a>
            <a href="/">Popular</a>
            <a href="/">Trending</a>
            <a href="/">Categories</a>
        </div>
    </div>
    </div>
{/if}



