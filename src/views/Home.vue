<template>
  <v-app>
    <NavBar />

    <v-main>

      <v-container>

        <v-row>

          <v-col cols="12" sm="12">

            <v-carousel>
              <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover>

                <v-row >

                  <v-col cols="12" sm="6">
                    <div class="d-flex fill-height justify-center">
                      <h2 class="text-white top">{{ item.title }}</h2>
                    </div>

                    <div class="d-flex fill-height justify-center">
                      <p class="text-white text">{{ item.text }}</p>
                    </div>

                    <div class="d-flex fill-height justify-center">
                      <v-btn class="button">Buy Now</v-btn>
                    </div>
                  </v-col>

                </v-row>

              </v-carousel-item>
            </v-carousel>

          </v-col>

          <v-toolbar color="transparent">
            <v-toolbar-title>Popular Products</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon="mdi mdi-chevron-left"></v-btn>
            <v-btn icon="mdi mdi-chevron-right"></v-btn>
          </v-toolbar>

          <v-col cols="12" sm="12" class="mt-n10">
            <Popular />
          </v-col>

          <v-toolbar color="transparent">
            <v-toolbar-title>Featured Products</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon="mdi mdi-chevron-left"></v-btn>
            <v-btn icon="mdi mdi-chevron-right"></v-btn>
          </v-toolbar>

          <v-col cols="12" sm="12" class="mt-n10">
            <Featured />
          </v-col>

        </v-row>

      </v-container>

    </v-main>

  </v-app>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

import NavBar from '@/components/NavBar.vue'
import Popular from '@/components/Popular.vue'
import Featured from '@/components/Featured.vue'

interface Item {
  src: string,
  title: string,
  text: string
}

const items = ref<Array<Item>>([])

items.value = [
  {
    src: "7.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
  {
    src: "1.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
  {
    src: "2.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
  {
    src: "3.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
  {
    src: "4.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
  {
    src: "5.jpg",
    title: "Surface Studio",
    text: "Le lorem ipsum est, en imprimerie, une suite de mots sans signification utilisée à titre provisoire pour calibrer une mise en page, le texte définitif venant remplacer le faux-texte dès ",
  },
]

</script>

<style scoped>
.top {
  margin-top: 6.25rem;
}

.text {
  margin-top: -2.5rem;
  margin-left: 5rem;
}

.top-day {
  margin-top: 7.5rem
}

.button {
  margin-top: -7.5rem;
}
</style>
