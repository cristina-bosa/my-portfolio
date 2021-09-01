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
    <div class="grid grid-cols-1 dark:bg-gray-800">
      <div class="presentation">
        <p class="text-black text-center dark:text-gray-300">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem
          quod reiciendis perferendis nesciunt eius! Possimus eos, illum, rerum
          ipsam quaerat repellendus beatae aliquam iste repellat itaque,
          voluptate perspiciatis aperiam debitis.
        </p>
      </div>
      <div class="skills">
        <div class="designer">
          <h3>Diseño</h3>
          <p>Siempre opto por estructuras limpias</p>
          <p>Lo que me encanta diseñar:</p>
          <p>UX, UI, Web, Móvil, Apps, Logos</p>
        </div>
        <div class="front">
          <h3>Front-end</h3>
          <p>Estructuras limpias</p>
          <p>Lenguajes:</p>
          <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>Sass</li>
          </ul>
          <p>Bases de datos:</p>
          <ul>
            <li>Mongo DB</li>
            <li>Maria DB</li>
          </ul>
          <p>Framework</p>
          <ul>
            <li>Vue 3</li>
            <li>Laravel</li>
            <li>Angular JS</li>
            <li>TailwindCSS</li>
            <li>Bootstrap 4</li>
          </ul>
        </div>
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
header {
  background-image: url("https://images.pexels.com/photos/2471235/pexels-photo-2471235.jpeg?cs=srgb&dl=pexels-luis-quintero-2471235.jpg&fm=jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
