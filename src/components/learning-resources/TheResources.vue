<template>
  <base-card>
    <base-button @click="setSelectedTab('stored-resources')"
      >Stored Resources</base-button
    >
    <base-button @click="setSelectedTab('add-resources')"
      >Add Resources</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import AddResources from './AddResources.vue';
import StoredResources from './StoredResources.vue';

export default {
  components: {
    AddResources,
    StoredResources,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
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
  provide() {
    return {
      resources: this.storedResources,
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>