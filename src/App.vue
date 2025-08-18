<script setup lang="ts">
const skills = [
  'Typescript', 'Javascript(ES6+)', 'Vue.js', 'React', 'Redux', 'Node.js', 'GraphQL', 'Express',
  'SQL', 'Docker', 'AWS', 'Git', 'CI/CD', 'Tailwind CSS', 'HTML5', 'CSS3', 'Figma'
];

const resumeUrl = `${import.meta.env.BASE_URL}Lead%20Full%20Software%20Engineer.pdf`

const projects = [
  {
    title: "PromptCraft App",
    description: "A sleek React-based app that helps users generate titles, summaries, rephrases, and more using the ChatGPT API.",
    image: "PromptCraft.png",
    github: "https://github.com/shravanthivr/PromptCraft",
  },
  {
    title: "Search Component",
    description: "Search Component to search medicines with autocomplete and suggestions.",
    image: "Project2.png",
    github: "https://github.com/shravanthivr/SearchComponent",
  },
  {
    title: "Weather App",
    description: "Weather App to fetch and display current weather data using OpenWeatherMap API.",
    image: "Project3.png",
    github: "https://github.com/shravanthivr/weatherapp-react",
  }
];
</script>

<template>
  <!-- Hero Section -->
  <section id="hero" class="bg-gradient-to-r from-cyan-500 to-teal-600 text-white py-20 px-6 text-center shadow-lg">
    <h1 class="text-5xl md:text-7xl font-extrabold mb-4 animate-fadeIn">
      Hello, I'm <span class="text-yellow-200">Shravanthi</span>
    </h1>
    <p class="text-xl md:text-2xl text-gray-100 mb-8">
      Senior Full Stack Engineer
    </p>
    <div class="flex justify-center gap-4">
      <a href="https://github.com/shravanthivr?tab=repositories" target="_blank"
        class="bg-white text-teal-700 font-bold py-3 px-6 rounded-lg hover:bg-gray-200 transition duration-300 shadow-md">
        View My Work
      </a>
      <a :href="resumeUrl"
      download="Shravanthi_Vadrevu_Resume.pdf"
      class="bg-yellow-400 text-teal-900 font-bold py-3 px-6 rounded-lg hover:bg-yellow-500 transition duration-300 shadow-md">
      Download Resume
    </a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="bg-gray-50 py-16 px-6 md:px-20 text-center shadow-inner">
    <h2 class="text-3xl font-bold mb-6">About Me</h2>
    <div class="md:flex items-center justify-center gap-8">
      <p class="text-gray-700 leading-relaxed max-w-xl mx-auto">
        I am a passionate and experienced Full Stack Engineer with a love for building elegant and efficient solutions.
        With over 11+ years in the industry, I have a proven track record of designing, developing, and deploying
        complex web applications. I thrive in collaborative environments and am always eager to learn and adapt
        to new technologies. My goal is to create software that is not only functional but also provides
        a seamless user experience.
      </p>
    </div>
  </section>


  <section id="skills" class="py-20 px-6 md:px-20 text-center">
    <h2 class="text-4xl font-bold text-center mb-12">Technical Skills</h2>
    <div class="flex flex-wrap justify-center items-center gap-8">
      <span v-for="skill in skills" :key="skill"
        class="bg-gradient-to-r from-cyan-500 to-teal-600 text-white px-4 py-2 rounded-full shadow hover:scale-105 transition">
        {{ skill }}
      </span>
    </div>
  </section>

  <section id="projects" class="py-20 bg-gray-100">
    <h2 class="text-4xl font-bold text-center mb-12">My Projects</h2>
    
    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3 max-w-6xl mx-auto px-4">
      <div 
        v-for="(project, index) in projects" 
        :key="index" 
        class="bg-white rounded-xl shadow-[-7px_15px_7px_-5px_rgba(0,_0,_0,_0.7)] overflow-hidden hover:shadow-2xl transition duration-300"
      >
        <img :src="project.image" :alt="project.title" class="w-full h-48 mt-2 object-contain">
        
        <div class="p-6">
          <h3 class="text-xl font-semibold mb-2">{{ project.title }}</h3>
          <p class="text-gray-600 mb-4">{{ project.description }}</p>
          
          <div class="flex space-x-4">
            <a 
              :href="project.github" 
              target="_blank" 
              class="bg-gray-800 text-white px-4 py-2 rounded-lg hover:bg-gray-900 transition duration-300"
            >
              GitHub
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="newsletter" class="py-20 bg-gray-50">
    <h2 class="text-4xl font-bold text-center mb-12">Subscribe to my Newsletter</h2>
    <div class="flex justify-center">
      <iframe src="https://shravanthivr.substack.com/embed" width="480" height="320" style="border:1px solid #EEE; background:white;" frameborder="0" scrolling="no"></iframe>
    </div>
  </section>

  <footer class="text-center py-6 text-gray-500">
    <p>&copy; {{ new Date().getFullYear() }} Shravanthi. All rights reserved.</p>
  </footer>

  <!-- Contact Floating Box -->
  <div id="contact"
    class="fixed top-1/3 right-4 bg-gray-900 text-white p-4 rounded-lg shadow-lg flex flex-col items-center gap-3">
    <span class="font-bold text-sm">Contact</span>
    <a href="mailto:shravanthivadrevu@gmail.com" title="Email" class="hover:text-cyan-400">
      <i class="fas fa-envelope text-xl"></i>
    </a>
    <a href="https://github.com/shravanthivr" target="_blank" title="GitHub" class="hover:text-cyan-400">
      <i class="fab fa-github text-xl"></i>
    </a>
    <a href="https://www.linkedin.com/in/shravanthi-vadrevu-radha/" target="_blank" title="LinkedIn"
      class="hover:text-cyan-400">
      <i class="fab fa-linkedin text-xl"></i>
    </a>
  </div>
</template>
