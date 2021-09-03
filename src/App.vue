<template>
  <header class="h-screen flex justify-center justify-items-center">
    <nav>
      <button v-if="isDark === true" @click="isDark = !isDark">
        <SunIcon class="h-5 w-5 text-black-700" />
      </button>
      <button v-else @click="isDark = !isDark">
        <MoonIcon class="h-5 w-5 text-black-700" />
      </button>
    </nav>

    <h1 class="text-center text-5xl text-white">
      Designer & Front-end developer
    </h1>
  </header>
  <main :class="isDark ? 'dark' : ''">
    <div class="dark:bg-gray-800">
      <div class="container mx-auto">
        <section class="pt-40 pb-40">
          <h2 class="text-2xl text-blue-400 text-center mb-5 dark:text-white">Hola, soy Cristina. Encantada de conocerte</h2>
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
import { MoonIcon, SunIcon } from "@heroicons/vue/outline";
export default {
  name: "App",
  components: {
    MoonIcon,
    SunIcon,
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
  background-image: url("https://images.pexels.com/photos/2471235/pexels-photo-2471235.jpeg?cs=srgb&dl=pexels-luis-quintero-2471235.jpg&fm=jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
