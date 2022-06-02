<template>
  <v-form>
    <v-sheet width="1000" color="#fafafa" elevation="3" class="pa-6">
      <v-container>
        <v-row>
          <v-col cols="4" class="pa-0 pr-4">
            <v-text-field
              v-model="surname"
              label="Фамилия"
              outlined
              clearable
            />
          </v-col>
          <v-col cols="4" class="pa-0 pr-4">
            <v-text-field
              v-model="firstname"
              label="Имя"
              outlined
              clearable
            />
          </v-col>
          <v-col cols="4" class="pa-0">
            <v-text-field
              v-model="secondname"
              label="Отчество"
              outlined
              clearable
            />
          </v-col>
        </v-row>

        <v-row>
          <v-text-field
            v-model="bachelor"
            label="Предшествующее образование"
            outlined
            clearable
          />
        </v-row>

        <v-row>
          <v-file-input
            v-model="courses"
            chips
            counter
            multiple
            show-size
            truncate-length="50"
            label="Дополнительные курсы подготовки"
            class="pa-0"
          />
        </v-row>

        <v-row>
          <v-file-input
            v-model="avegareScores"
            chips
            show-size
            truncate-length="50"
            label="Cредние оценки по блокам дисциплин "
          />
        </v-row>

        <v-row>
          <v-textarea
            v-model="vacancy"
            outlined
            label="Опишите свои планируемые вакансии"
            height="120"
          />
        </v-row>

        <v-row>
          <v-file-input
            v-model="science"
            chips
            show-size
            multiple
            counter
            truncate-length="50"
            label="Научная деятельность"
            class="pa-0 mb-3"
          />
        </v-row>

        <v-row>
          <v-textarea
            v-model="work"
            outlined
            label="Расскажите о своей трудовой деятельности"
            height="120"
          />
        </v-row>

        <v-row>
          <v-file-input
            v-model="olympics"
            chips
            show-size
            multiple
            counter
            truncate-length="50"
            label="Олимпиады"
            class="pa-0 mb-3"
          />
        </v-row>

        <v-btn color="primary" @click="test">Отправить</v-btn>
      </v-container>
    </v-sheet>
  </v-form>
</template>

<script>

import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class FormPage extends Vue {
  surname = ''
  firstname = ''
  secondname = ''
  bachelor = ''
  courses = []
  avegareScores = null
  vacancy = ''
  science = []
  work = ''
  olympics = []

  test() {
    // console.log(this.avegareScores)
  }
}
</script>
