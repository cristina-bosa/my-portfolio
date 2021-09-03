<template>
  <header :class="isDark ? 'dark' : ''">
    <nav class="p-3 m-0 w-full flex flex-row flex-wrap bg-white dark:bg-gray-800">
      <div class="w-1/5 flex flex-row flex-wrap justify-center content-center">
        <h2>Cristina</h2>
      </div>

      <div id="nav-items" class="sm:border-l-4 md:border-none border-indigo-400 transition close sm:pt-16 md:pt-0 sm:h-full md:h-auto sm:absolute sm:right-0 sm:top-0 md:top-auto md:right-auto md:relative md:w-4/5 sm:bg-gray-900 sm:text-white md:text-gray-500 md:bg-transparent md:flex flex flex-row flex-wrap justify-center sm:content-start md:content-center">
      <button v-if="isDark === true" @click="isDark = !isDark">
        <SunIcon class="h-5 w-5 text-black-700" />
      </button>
      <button v-else @click="isDark = !isDark">
        <MoonIcon class="h-5 w-5 text-black-700" />
      </button>
  </div>

    </nav>

      <div class="h-screen flex justify-center items-center">
        <h1 class="text-center font-extrabold text-5xl text-white">Designer & Front-end developer</h1>
        <a href="#presentation" class="text-center"><ArrowNarrowDownIcon class="h-5 w-5 text-black-700" /></a>
      </div>

  </header>
  <main :class="isDark ? 'dark' : ''">
    <div class="dark:bg-gray-800">
      <div class="container mx-auto">
        <section class="pt-40 pb-40" id="presentation">
          <h2 class="text-2xl text-blue-400 font-bold text-center mb-5 dark:text-white">Hola, soy Cristina. Encantada de conocerte</h2>
          <p class="text-gray-800 text-center dark:text-gray-400">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem
            quod reiciendis perferendis nesciunt eius! Possimus eos, illum,
            rerum ipsam quaerat repellendus beatae aliquam iste repellat itaque,
            voluptate perspiciatis aperiam debitis.
          </p>
        </section>
        <section class="grid grid-cols-2">
          <div>
            <h3 class="text-xl text-blue-400 text-center mb-5 dark:text-white">Diseño</h3>
            <p class="text-gray-800 text-center dark:text-gray-400">Siempre opto por estructuras limpias</p>
            <p class="text-gray-800 text-center dark:text-gray-400">Lo que me encanta diseñar:</p>
            <p class="text-gray-800 text-center dark:text-gray-400">UX, UI, Web, Móvil, Apps, Logos</p>
          </div>
          <div>
            <h3 class="text-xl text-blue-400 text-center mb-5 dark:text-white">Front - end</h3>
            <p class="text-gray-800 text-center dark:text-gray-400">Estructuras limpias</p>
            <p class="text-gray-800 text-center dark:text-gray-400">Lenguajes:</p>
            <ul>
              <li class="text-gray-800 text-center dark:text-gray-400">HTML</li>
              <li class="text-gray-800 text-center dark:text-gray-400">CSS</li>
              <li class="text-gray-800 text-center dark:text-gray-400">Sass</li>
            </ul>
            <p class="text-gray-800 text-center dark:text-gray-400" >Bases de datos:</p>
            <ul>
              <li class="text-gray-800 text-center dark:text-gray-400">Mongo DB</li>
              <li class="text-gray-800 text-center dark:text-gray-400">Maria DB</li>
            </ul>
            <p class="text-gray-800 text-center dark:text-gray-400" >Framework</p>
            <ul>
              <li class="text-gray-800 text-center dark:text-gray-400">Vue 3</li>
              <li class="text-gray-800 text-center dark:text-gray-400">Laravel</li>
              <li class="text-gray-800 text-center dark:text-gray-400">Angular JS</li>
              <li class="text-gray-800 text-center dark:text-gray-400">TailwindCSS</li>
              <li class="text-gray-800 text-center dark:text-gray-400">Bootstrap 4</li>
            </ul>
          </div>
        </section>
      </div>
    </div>
  </main>
</template>

<script>
import "./assets/tailwind.css";
import { MoonIcon, SunIcon, ArrowNarrowDownIcon } from "@heroicons/vue/outline";
export default {
  name: "App",
  components: {
    MoonIcon,
    SunIcon,
    ArrowNarrowDownIcon
  },
  data() {
    return {
      isDark: true,
    };
  },
};
</script>

<style>
header {
  background-image: url("https://images.pexels.com/photos/5186869/pexels-photo-5186869.jpeg?cs=srgb&dl=pexels-fiona-art-5186869.jpg&fm=jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
