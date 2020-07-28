<template>
  <q-page class="bg-grey-3 column">
    <q-list separator bordered class="bg-white">
      <q-item
        v-for="task in tasks"
        :key="task.title"
        :class="{ 'done bg-blue-1' : task.done }"
        tag="label"
        v-ripple
      >
        <q-item-section avatar>
          <q-checkbox v-model="task.done" color="primary"/>
        </q-item-section>
        <q-item-section>
          <q-item-label>{{ task.title }}</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        {
          title: 'Task 1',
          done: false
        },
        {
          title: 'Task 2',
          done: false
        },
        {
          title: 'task 3',
          done: false
        }
      ]
    }
  }
}
</script>

<style lang="scss" >
.done{
  .q-item__label{
    text-decoration: line-through;
    color: #bbb;
  }
}
</style>