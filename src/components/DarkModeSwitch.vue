<template>
  <div id="container vertical-center">
    <ion-grid>
        <ion-row class="ion-align-items-center">
            <ion-col size="2" class="ion-text-center"> <ion-icon :icon="sunny"/> </ion-col>
            <ion-col size="8" class="ion-text-center"> <ion-toggle :icon="moon" @ionChange="pindah" :checked="dark" mode="ios"/> </ion-col>
            <ion-col size="2" class="ion-text-center"> <ion-icon :icon="moon"/> </ion-col>
        </ion-row>
    </ion-grid>
  </div>
</template>

<script lang="ts">
import { IonToggle, IonIcon } from '@ionic/vue';
import { sunny, moon } from 'ionicons/icons';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ExploreContainer',
  components: {
    IonToggle,
    IonIcon
  },
  data: () => ({
    sunny,
    moon,
    dark: false,

  }),
  methods: {
    pindah(ev){
    //  console.log(window.matchMedia("(prefers-color-scheme: dark)").matches);
     document.body.classList.toggle('dark', ev.detail.checked);
    }
  },
  mounted(){
    // this.dark = window.matchMedia("(prefers-color-scheme: dark)").matches;
    document.body.classList.toggle('dark', false);
  }
})
</script>
<style scoped>
</style>