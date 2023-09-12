<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <v-card
      class="mx-auto"
      max-width="448"
    >
      <v-layout>
        <v-app-bar
          color="primary"
          density="compact"
        >
          <template v-slot:prepend>
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
          </template>
  
          <v-app-bar-title>Photos</v-app-bar-title>
  
          <template v-slot:append>
            <v-btn icon="mdi-dots-vertical"></v-btn>
          </template>
        </v-app-bar>

        <v-main>
          <v-container fluid>
            <v-row dense>
              <v-col
                v-for="n in 8"
                :key="n"
                cols="3"
              >
                <v-sheet
                  color="grey-lighten-2"
                  height="96"
                ></v-sheet>
              </v-col>
            </v-row>
          </v-container>
        </v-main>
      </v-layout>
    </v-card>

  <header>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

<div>
  <RouterView />
</div>

<div>footer</div>

</template>

<style scoped>

</style>
