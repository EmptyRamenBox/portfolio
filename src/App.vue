<template>
  <v-app>
    <v-container fill-height>
      <v-row justify="center" align="center">
        <v-col cols="12" class="text-center">
          <h1 class="display-4">Empty Ramen Studios Portfolio</h1>
        </v-col>
        <v-col cols="12" class="text-center">
          <p>amart439@stu.southtexascollege.edu</p>
        </v-col>
        <v-col>
          <v-container>
            <v-row justify="center">
              <v-col v-for="(project,index) in projects" :key="index">
                <v-card max-width="344" class="mx-auto">
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">{{project.name}}</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>

                  <v-img :src="project.screenshot" contain height="194"></v-img>

                  <v-card-text>{{project.description}}</v-card-text>

                  <v-card-actions>
                    <v-btn text color="blue darken-1" :href="project.url" target="_blank">Go To Site</v-btn>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-share-variant</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    projects: [
      {
        name: 'Vue Todo Application',
        description: 'A simple to do application that handles completed and pending tasks. It also keeps records of total tasks per bucket',
        screenshot: '/images/vue-todo.png',
        url: 'https://todo.collegeandcoffee.site'
      },
      {
        name: 'Marvel Finder',
        description: 'Using Marvel Public API, we have a simple character finder application, with character description and some comics where the character appears.',
        screenshot: '/images/marvelfinder.png',
        url: 'https://marvelfinder.collegeandcoffee.site'
      },
      {
        name: 'Super Awesome App',
        description: 'The coolest and better Social Network ever created (by me)',
        screenshot: '/images/superawesomeapp-prev.png',
        url: 'https://superawesomeapp.collegeandcoffee.site'
      }
    ]
  })
}
</script>
