<template>
  <the-header title="RememberMe"></the-header>
  <stored-resources :resources="storedResources"></stored-resources>
</template>

<script>
import TheHeader from './components/layout/TheHeader.vue';
import StoredResources from './components/learning-resources/StoredResources.vue';
export default {
  components: {
    TheHeader,
    StoredResources,
  },
  data() {
    return {
      storedResources: [
        {
          id: 1,
          title: 'Official Guide',
          description: 'The official vue js documentation',
          link: 'https://vuejs.org',
        },
        {
          id: 2,
          title: 'Google',
          description:
            'it is super important to learn google priror to learn anything',
          link: 'https://google.com',
        },
      ],
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>