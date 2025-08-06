<script setup lang="ts">
const skills = [
  'Typescript', 'Javascript(ES6+)', 'Vue.js', 'React', 'Node.js', 'Express',
  'SQL', 'Docker', 'AWS', 'Git', 'CI/CD', 'Tailwind CSS', 'HTML5', 'CSS3'
];
</script>

<template>
  <div class="container mx-auto p-4 md:p-8">
    <header class="flex justify-between items-center py-8">
      <div class="text-2xl font-bold text-cyan-400">My Portfolio</div>
      <nav class="hidden md:flex space-x-8">
        <a href="#about" class="hover:text-cyan-400 transition duration-300">About</a>
        <a href="#projects" class="hover:text-cyan-400 transition duration-300">Projects</a>
        <a href="#skills" class="hover:text-cyan-400 transition duration-300">Skills</a>
        <a href="#contact" class="hover:text-cyan-400 transition duration-300">Contact</a>
      </nav>
    </header>

    <main>
      <section id="hero" class="py-18">
        <h1 class="text-5xl md:text-7xl font-extrabold mb-4">
          Hello, I'm <span class="text-cyan-400">Shravanthi</span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-400 mb-8">A Senior Full Stack Engineer</p>
        <a
  href="https://github.com/shravanthivr?tab=repositories"
  target="_blank"
  rel="noopener noreferrer"
  class="bg-cyan-500 text-white font-bold py-3 px-6 rounded-lg hover:bg-cyan-600 transition duration-300"
>
  View My Work
</a>
      </section>

      <!-- About -->
      <section id="about" class="py-15">
        <h2 class="text-4xl font-bold text-center mb-8">About Me</h2>
        <div class="flex flex-col md:flex-row items-center">
          <div class="mb-8 md:mb-0">
            <p class="text-gray-600 leading-relaxed">
              I am a passionate and experienced Full Stack Engineer with a love for building elegant and efficient solutions.
              With over 11+ years in the industry, I have a proven track record of designing, developing, and deploying complex web applications.
              I thrive in collaborative environments and am always eager to learn and adapt to new technologies.
              My goal is to create software that is not only functional but also provides a seamless user experience.
            </p>
          </div>
        </div>
      </section>

      <!-- Projects 
      <section id="projects" class="py-20">
        <h2 class="text-4xl font-bold text-center mb-12">My Projects</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        </div>
      </section>-->

      <!-- Skills -->
      <section id="skills" class="py-20">
        <h2 class="text-4xl font-bold text-center mb-12">Technical Skills</h2>
        <div class="flex flex-wrap justify-center items-center gap-4">
          <span v-for="skill in skills" :key="skill" class="bg-gray-700 text-gray-200 text-lg font-medium px-4 py-2 rounded-full">
            {{ skill }}
          </span>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="py-20 text-center">
        <h2 class="text-4xl font-bold mb-4">Get in Touch</h2>
        <p class="text-gray-400 mb-8">I'm currently open to new opportunities. Feel free to reach out!</p>
        <a href="mailto:shravanthivadrevu@gmail.com" class="bg-cyan-500 text-white font-bold py-3 px-6 rounded-lg hover:bg-cyan-600 transition duration-300">
          Email me
        </a>
        <div class="flex justify-center space-x-6 mt-8">
  <a href="https://github.com/shravanthivr" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-white">
    <i class="fab fa-github fa-2x"></i>
  </a>
  <a href="https://www.linkedin.com/in/shravanthi-vadrevu-radha/" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-white">
    <i class="fab fa-linkedin fa-2x"></i>
  </a>
</div>
      </section>
    </main>

    <footer class="text-center py-8 text-gray-500">
      <p>&copy; {{ new Date().getFullYear() }} Shravanthi. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped></style>
