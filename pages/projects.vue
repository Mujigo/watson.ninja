<template>
  <v-container>
    <v-row>
      <v-col v-for="(project, index) in projects" :key="index" align-self="center">
        <v-card shaped max-width="300">
          <v-img :src="project.img" contain width="300" />
          <v-card-title>{{ project.name }}</v-card-title>
          <v-card-text>{{ project.description }}</v-card-text>
          <v-divider />
          <v-card-text>
            <v-btn :href="project.link" target="_blank">
              Check It Out!
            </v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          name: 'Save the Frogs',
          description: 'Save the Frogs is one of the projects I completed for the Udacity Front End Development course.',
          img: 'images/project-images/save-the-frogs.png',
          link: 'https://savethefrogs.watson.ninja'
        },
        {
          name: 'Memory Game',
          description: 'A Memory Game that was one of the project for the Udacity Front End Development course.',
          img: 'images/project-images/memory-game.png',
          link: 'https://memory.watson.ninja/'
        }
      ]
    }
  }
}
</script>

<style></style>
