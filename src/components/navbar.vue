<template>
    
    <div class="bg-gray-900 text-gray-100 py-3.5 px-6 shadow md:flex justify-between items-center">


<div class="flex items-center cursor-pointer">
   <span class="text-green-400 text-xl mr-1"><i class="bi bi-messenger"> </i> </span> 

<h1 class="text-xl"> Designer</h1>
</div>
<span @click="MenuOpen()" class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl">
  <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>

</span>
<ul class="md:flex md:items-center md:px-0 px-12 md:pb-0 pb-10 md:static absolute bg-gray-900 md:w-auto w-full top-14 duration-700 ease-in"
:class="[open ? 'left-0' : 'left-[-100%]']">


     <li class="md:mx-10 md:my-10 my-6" v-for="(link, index) in links" :key="index">
        <a :href="link.link" class="text-xl hover:text-green-500"> {{ link.Home }}</a>
    </li>
      <li class="md:mx-10  md:my-10 my-6">
        <a href="#" class="text-xl hover:text-green-500">Home</a>
    </li>
     <li class="md:mx-10  md:my-10 my-6">
        <a href="#" class="text-xl hover:text-green-500">Services</a>
    </li>
     <li class="md:mx-10  md:my-10 my-6">
        <a href="#" class="text-xl hover:text-green-500">About</a>
    </li>
     <li class="md:mx-10  md:my-10 my-6">
        <a href="#" class="text-xl hover:text-green-500">Blog</a>



    </li>
     <li class="md:mx-10  md:my-10 my-6">
        <a href="#" class="text-xl hover:text-green-500">Contact</a>
    </li>


    <Button>
        Get started
         </Button>
        
</ul>
    </div>

</template>

<script>
import { ref } from 'vue';

import Button from './Button.vue'

export default {
    components:{
        Button
       
    },
  setup() {

    let open = ref(false)
    const links = [
      { name: "Home", link: "#" },
      { name: "Services", link: "#" },
      { name: "About", link: "#" },
      { name: "Blog", link: "#" },
      { name: "Contact", link: "#" }
    ];
function MenuOpen(){
  open.value = !open.value
}
    return {
      links,open,MenuOpen
    };
  }
}
</script>

