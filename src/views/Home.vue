<template>
  <v-app>
    <NavBar />

    <v-main>

      <v-container>

        <v-col cols="12" sm="12">

          <v-carousel>
            <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover>

            </v-carousel-item>
          </v-carousel>

        </v-col>

      </v-container>

    </v-main>

  </v-app>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

import NavBar from '@/components/NavBar.vue'

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
