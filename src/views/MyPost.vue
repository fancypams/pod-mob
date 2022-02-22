<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">I just listened to...</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-grid>
        <ion-row>
          <ion-input placeholder="Add podcast name"></ion-input>
        </ion-row>
        <ion-row>
          <ion-select multiple="true" cancel-text="Cancel" ok-text="Select" placeholder="Select episode">
            <ion-select-option value="bacon">Bacon</ion-select-option>
          </ion-select>
        </ion-row>
        <ion-row>
          <ion-text>How much did you like this one?</ion-text>
          <div class="star-rating-input">
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="starHalfOutline" class="star-rating-default"></ion-icon>
            <ion-icon :icon="starOutline" class="star-rating-default"></ion-icon>
          </div>
        </ion-row>
        <ion-row>
          <ion-textarea placeholder="Add your thoughts on this episode"></ion-textarea>
        </ion-row>
        <ion-row>
          <ion-button>Share</ion-button>
        </ion-row>
      </ion-grid>

      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Your friends just posted...</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <ion-card>
        <ion-card-header>
          <div>
            <ion-card-subtitle>Card Subtitle</ion-card-subtitle>
            <ion-card-title>Card Title</ion-card-title>
          </div>
          <div>
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="star" class="star-rating-default"></ion-icon>
            <ion-icon :icon="starHalfOutline" class="star-rating-default"></ion-icon>
            <ion-icon :icon="starOutline" class="star-rating-default"></ion-icon>
          </div>
        </ion-card-header>

        <ion-card-content>
          Keep close to Nature's heart... and break clear away, once in awhile,
          and climb a mountain or spend a week in the woods. Wash your spirit clean.
        </ion-card-content>
      </ion-card>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonIcon } from '@ionic/vue';
import { star, starOutline, starHalfOutline } from 'ionicons/icons';

export default  defineComponent({
  name: 'MyPost',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonIcon },
  setup() {
    return {
      star,
      starOutline,
      starHalfOutline
    }
  }
});
</script>

<style scoped>
  .star-rating-input {
    width: 43%;
    text-align: end;
  }
</style>
