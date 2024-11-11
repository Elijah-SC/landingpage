<!-- <script setup>

</script>

<template>
  <div class="hero-bg container-fluid">
    <div class="row">
      <div class="col-8 d-flex flex-column justify-content-center text-primary">
        <h1 class="name">Elijah SasserCollins</h1>
        <h1 class="hero-text">FullStack-Developer</h1>
      </div>
      <div class="col-4">
        <img src="/img/MeNoBg.png" alt="Elijah SasserCollins" class="me">
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.hero-bg {
  background-color: var(--bs-body-bg);
  height: 100vh;
}

.name {
  font-size: 100px;
  }
  

  .me {
    width: 100%;
    object-fit: cover;
    object-position: center;
    border-radius: 40%;
    }
    </style> -->

<template>
  <div id="app" class="victor-mono">
    <!-- Header Section -->
    <header class="header container-fluid">
      <div class="largeSc-card row justify-content-between align-items-center flex-grow-1">
        <div class="text-content col-md-7">
          <h1 class="title victor-mono">Hi, I'm Elijah</h1>
          <h1 class="last victor-mono">SasserCollins</h1>
          <p class="subtitle">Software Developer | Javascript, .Net, C#, Vue, Node, MySQL</p>
          <button class="contact-btn" @click="scrollToContact">Contact Me</button>
        </div>
        <div class="image-content col-md-4">
          <img src="/img/MeNoBg.png" alt="Your Photo" class="profile-pic" />
        </div>
      </div>
      <div class="smallSc-card justify-content-between align-items-center bg-success p-2 rounded">
        <div class="image-smallSc">
          <img src="/img/MeNoBg.png" alt="Your Photo" class="profile-pic" />
        </div>
        <div>
          <h1 class="mb-0">Elijah SasserCollins</h1>
          <p>Full Stack Software-Developer</p>
          <div>
            <a href="">
              <i class="mdi mdi-github"></i>
            </a>
            <a href="https://www.linkedin.com/in/elijah-sassercollins/">
              <i class="mdi mdi-linkedin"></i>
            </a>
          </div>
        </div>

      </div>
    </header>

    <!-- About Section -->
    <section class="about" id="about">
      <h2>About Me</h2>
      <p>
        I'm a passionate developer skilled in [Technologies/Skills]. I love building efficient, scalable, and
        user-friendly applications.
      </p>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
      <h2>Projects</h2>
      <div class="project-list">
        <div v-for="project in projects" :key="project.name" class="project-card">
          <h3>{{ project.name }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" target="_blank" class="project-link">View Project</a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <h2>Contact</h2>
      <p>Feel free to reach out via email at <a :href="'mailto:' + email">{{ email }}</a></p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        { name: 'Project One', description: 'Description for project one.', link: 'https://example.com' },
        { name: 'Project Two', description: 'Description for project two.', link: 'https://example.com' },
      ],
      email: 'your.email@example.com',
    };
  },
  methods: {
    scrollToContact() {
      document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>
#app {
  background-color: #000000;
  /* Black background */
  color: #ffffff;
  /* White text */
  line-height: 1.6;
  text-align: center;
}

/* Header Section */
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 100px 20px;
  color: #00bfff;
  /* Light blue for text */
}



.text-content {
  flex: 1;
  padding-right: 20px;
}

.title {
  font-size: 4em;
  font-weight: 600;
  color: #00bfff;
  text-align: start;
  margin: unset;
  /* Light blue */
}

.last {
  font-size: 4em;
  font-weight: 600;
  color: #00bfff;
  text-align: center;
  /* Light blue */
}

.subtitle {
  font-size: 1.5em;
  margin-bottom: 20px;
}

.contact-btn {
  padding: 10px 20px;
  font-size: 1em;
  color: #000000;
  /* Black button text */
  background-color: #00bfff;
  /* Light blue button */
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.contact-btn:hover {
  background-color: #1e90ff;
  /* Darker blue on hover */
}

.image-content {
  display: flex;
  justify-content: end;
  margin-right: 30px;

}

@media (max-width: 768px) {
  .image-content {
    justify-content: space-around;

  }

}

@media (max-width: 768px) {
  .largeSc-card {
    display: none;

  }

}

.smallSc-card {
  display: none;
}

@media (max-width: 768px) {
  .smallSc-card {
    display: flex;

  }

}


.profile-pic {
  width: 100%;
  max-width: 300px;
  border-radius: 40%;
}

/* About Section */
.about {
  padding: 60px 20px;
  color: #00bfff;
  /* Light blue for section headers */
}

/* Projects Section */
.projects {
  padding: 60px 20px;
}

.project-list {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.project-card {
  background-color: #333333;
  /* Dark gray card background */
  color: #ffffff;
  /* White text */
  padding: 20px;
  border-radius: 8px;
  width: 300px;
}

.project-link {
  color: #00bfff;
  /* Light blue links */
  text-decoration: none;
  font-weight: bold;
}

.project-link:hover {
  text-decoration: underline;
}

/* Contact Section */
.contact {
  padding: 60px 20px;
  color: #00bfff;
  /* Light blue for links */
}

.contact a {
  color: #00bfff;
  /* Light blue for links */
  text-decoration: none;
}

.contact a:hover {
  text-decoration: underline;
}
</style>