<template>
  <div class="border  p-8">
    <header class=" bg-slate-500 mb-12 md:flex justify-around">
    
      <h1 class="text-4xl font-bold mt-10">BRIAN MWANGI</h1>
      <p class="text-lg text-gray-600 mt-28">Welcome to my personal profile</p>

        <div>
      <ul>
        <li class="mt-4">
        <a href="#"><i class="bi bi-envelope"></i> yobrahmwas29@gmail.com</a>
    </li>
        <li class="mt-4">
        <a href="#"><i class="bi bi-linkedin"></i> Linkedin</a>
    </li>
       <li class="mt-4">
        <a href="#"><i class="bi bi-github"></i> Github</a>
    </li>
      </ul>
      </div>
    </header>

    <div class="md:flex justify-around ">
      <img
        src="../assets/dev.png"
        class="w-96 h-96 object-cover "
      />

      <div class="border bg-gray-200 p-10">
        <h1 class="font-bold text-3xl">
          About <span class="text-slate-700">me</span>
        </h1>

        <p class="mt-8 ">
          "I am a dedicated software engineer  based on <br>front-end developer 
          with a strong background<br> in 
          developing innovative software solutions.<br>
          My passion lies in solving complex problems and <br>
          creating applications that enhance user experiences <br>
          and drive business success."
        </p>
      </div>
    </div>

    <div class="border bg-gradient-to-r from-green-400 via-blue-500 to-purple-600 p-10 mt-10">
      <h2 class="font-semibold text-4xl"> projects</h2>
    <section class=" bg-blue-400 md:grid-cols-4 lg:grid-cols-3 gap-8 mt-14 ">
      <div
        v-for="project in projects"
        :key="project.id"
        class=" p-6 rounded-lg shadow-lg mt-7"
      >
        <h2 class="text-2xl font-semibold mb-2 mt-7">{{ project.title }}</h2>
        <p class="text-gray-200 mt-9">{{ project.description }}</p>
      </div>

    </section>

       <p class="text-center mt-10 text-4xl"> #Devepoler ...</p>
</div>


    
  </div>
</template>

<script>
export default {
  name: "Portfolio",
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "Project 1",
          description: "company site project.",
        },
        {
          id: 2,
          title: "Project 2",
          description: "housing project .",
        },
        {
          id: 3,
          title: "Project 3",
          description: "A project on python based on data visualization full project.",
        },
        {
          id: 3,
          title: "Project 4",
          description: "A project on SQL on data manipulations and retrieval .",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Add any additional styles here */
</style>
