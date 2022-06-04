<template>
  <div class="d-flex align-center flex-wrap">
    <v-list>
      <v-card
        v-for="student in students"
        :key="student.id"
      >
        <v-card-title>
          {{ student.name }}
        </v-card-title>
        <v-card-actions>
          <v-btn>Изменить</v-btn>
          <v-btn @click="handleClickDelete">Удалить</v-btn>
        </v-card-actions>
      </v-card>
    </v-list>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class RecommendationsPage extends Vue {
  students = [
    {
      id: '1',
      name: 'Иванов',
      data: {}
    },
    {
      id: '2',
      name: 'Петров',
      data: {}
    },
    {
      id: '3',
      name: 'Сидоров',
      data: {}
    },
  ]

  handleClickDelete(deleteStudent: { id: string, name: string, data: any }) {
    this.students = this.students.filter((student) => student.id !== deleteStudent.id)
  }
}
</script>
