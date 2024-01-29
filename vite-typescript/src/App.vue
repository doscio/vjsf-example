<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row>
          <v-col>
            <p>Runtime compilation</p>
            <p>{{ person1 }}</p>
            <v-form>
              <vjsf
                v-model="person1"
                :schema="personSchema"
                :options="options"
              />
            </v-form>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import personSchema from './schemas/person.json'
import Vjsf from '@koumoul/vjsf'

const person1 = ref<any>(null)
const options = {}
</script>
