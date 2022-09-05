<template>
  <div class="app-home">
    <v-card max-width="600" class="mx-auto" color="grey-lighten-3">
      <v-layout>
        <v-app-bar color="teal-darken-4">
          <template v-slot:image>
            <v-img gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"></v-img>
          </template>

          <template v-slot:prepend>
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          </template>

          <v-app-bar-title>Nuxt Vuetify Boilerplate</v-app-bar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-heart</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" temporary>
          <v-row align="center" justify="center" class="mt-5">
            <v-avatar color="primary" size="56" class=" font-weight-bold">NB</v-avatar>
            <span class="ml-2 font-weight-bold">Boilerplate</span>
          </v-row>
        </v-navigation-drawer>

        <v-main>
          <v-container fluid>
            <v-row dense>
              <v-col v-for="n in 4" :key="n" cols="6">
                <v-card :title="`Content ${n}`" :subtitle="`Subtitle for Content ${n}`"
                  text="Lorem ipsum dolor sit amet consectetur, adipisicing elit.?"></v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-main>
      </v-layout>
    </v-card>
  </div>
</template>
<script>
export default defineComponent({
  data() {
    return {
      drawer: null,
    }

  },
})
</script>

