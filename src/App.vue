<template>
  <v-app>
    <v-main>
      <templateTask/>
    </v-main>
  </v-app>
</template>

<script>
import templateTask from './components/templateTask';

export default {
  name: 'App',

  components: {
    templateTask,
  },

  data: () => ({
    //
  }),
};
</script>
