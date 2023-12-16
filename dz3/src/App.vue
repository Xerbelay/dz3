<template>
  <ul>
    <li v-for="i, b in workers" :key="i.id">
      {{ 'Имя: ' + i.name }}
      <ul>
        <li>
          {{ 'Зарплата: ' + i.salary }}
        </li>
        <li>
          {{ 'Должность: ' + i.job }}
        </li>
        <li>
          {{ 'id: ' + i.id }}
        </li>
      </ul>
      <button @click="deleteItem(b)">Удалить сотрудника</button>
    </li>
  </ul>
<button @click="create">Добавить сотрудника</button>
<ul v-for="i, b in workers" :key="i.id">
  <li>
    {{ 'Зарплата: ' + i.salary }}
  </li>
  <li>
    {{ 'Должность: ' + i.job }}
  </li>
  <li>
    {{ 'id: ' + i.id }}
  </li>
</ul>
</template>

<script>
export default {
  data(){
    return{
      workers: [
        {
          id: 1,
          name: 'Арина',
          salary: 0,
          job: 'уборщица'
        },
        {
          id: 2,
          name: 'Иван',
          salary: 1000,
          job: 'уборщик'
        },
        {
          id: 3,
          name: 'Владислав',
          salary: 5000,
          job: 'уборщик'
        },
      ],
      John: {
        id: 1,
        name: 'John',
        salary: 0,
        job: 'сотрудник'
      }
    }
  },
  computed: {

  },
  methods: {
    deleteItem(b){
      this.workers.slice(b,1)
    },
    create(){
      template.append(this.john)
    }
  }
}
</script>

<style>

</style>
