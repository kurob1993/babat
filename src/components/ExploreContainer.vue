<template>
  <div id="container">
    <strong>{{ name }}</strong>
    <p>Explore <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
    
    <div class="p-6 max-w-sm mx-auto bg-white dark:bg-gray-800 rounded-xl shadow-md flex items-center space-x-4">
      <div class="flex-shrink-0">
        <ion-icon :icon="sunny" class="h-12 w-12" />
      </div>
      <div>
        <div class="text-xl font-medium text-black dark:text-white">ChitChat</div>
        <p class="text-gray-500">You have a new message!</p>
      </div>
    </div>
    
  </div>
</template>

<script lang="ts">
import { IonIcon } from '@ionic/vue';
import { sunny } from 'ionicons/icons';
export default {
  name: 'ExploreContainer',
  components:{
    IonIcon
  },
  props: {
    name: String
  },
  data: () => ({
    sunny
  })
}
</script>

<style scoped>
#container {
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>