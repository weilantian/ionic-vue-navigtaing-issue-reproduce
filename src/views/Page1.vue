<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
         <ion-buttons slot="secondary">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Page 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Page 1</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-button @click="router.push('/page2')" expand="block">Push to Page 2</ion-button>
    
      <ExploreContainer name="Page 1" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent,IonBackButton,IonButtons,IonButton } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { useRouter } from 'vue-router';

export default  {
  name: 'Tab1',
  components: { ExploreContainer, IonHeader, IonToolbar, IonTitle, IonContent, IonPage,IonBackButton,IonButtons,IonButton },
  setup() {
    const router = useRouter()
    return {router}
  }
}
</script>