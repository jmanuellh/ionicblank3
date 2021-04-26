<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <div>
          <!-- Default -->
          <ion-button>Default</ion-button>

          <!-- Anchor -->
          <ion-button href="#">Anchor</ion-button>

          <!-- Colors -->
          <ion-button color="primary">Primary</ion-button>
          <ion-button>
            <ion-icon name="add"></ion-icon>
          </ion-button>
          <ion-button color="secondary">Secondary</ion-button>
          <ion-button>
            <ion-icon slot="start" name="star"></ion-icon>
            Left Icon
          </ion-button>
        </div>
        <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButton, IonIcon } from '@ionic/vue';
import { addIcons } from "ionicons";
import { star, add } from 'ionicons/icons';

addIcons({
  // "ios-map": map.ios,
  // "md-map": map.md,
  // "md-star": star.md,
  star,
  add
});

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton,
    IonIcon
  }
});
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