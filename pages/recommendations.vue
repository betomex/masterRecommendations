<template>
  <div>
    <h1 class="mb-12">Рекомендации направление - студент</h1>
    <v-data-table
      disable-pagination
      disable-sort
      hide-default-footer
      :headers="headers"
      :items="specialities"
      class="elevation-6"
    >
      <template v-slot:item.petrov="{ item }">
        <v-simple-checkbox
          v-model="item.petrov"
          disabled
        />
      </template>
      <template v-slot:item.ivanov="{ item }">
        <v-simple-checkbox
          v-model="item.ivanov"
          disabled
        />
      </template>
      <template v-slot:item.sidorov="{ item }">
        <v-simple-checkbox
          v-model="item.sidorov"
          disabled
        />
      </template>
      <template v-slot:item.vasilieva="{ item }">
        <v-simple-checkbox
          v-model="item.vasilieva"
          disabled
        />
      </template>
      <template v-slot:item.igoreva="{ item }">
        <v-simple-checkbox
          v-model="item.igoreva"
          disabled
        />
      </template>
    </v-data-table>
  </div>
</template>

<script>
import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class RecommendationsPage extends Vue {
  headers = [
    { text: '', align: 'start', value: 'name', },
    { text: 'Петров', value: 'petrov' },
    { text: 'Иванов', value: 'ivanov' },
    { text: 'Сидоров', value: 'sidorov' },
    { text: 'Васильева', value: 'vasilieva' },
    { text: 'Игорёва', value: 'igoreva' }
  ]

  specialities = [
    {
      name: '01.04.02 КИТ',
      petrov: false,
      ivanov: false,
      sidorov: true,
      vasilieva: false,
      igoreva: false
    },
    {
      name: '01.04.02 КПМ',
      petrov: false,
      ivanov: true,
      sidorov: false,
      vasilieva: true,
      igoreva: false
    },
    {
      name: '01.04.02 КММ',
      petrov: false,
      ivanov: true,
      sidorov: false,
      vasilieva: false,
      igoreva: false
    },
    {
      name: '02.04.02',
      petrov: false,
      ivanov: false,
      sidorov: true,
      vasilieva: false,
      igoreva: false
    }
  ]
}
</script>
