<template>
  <v-row justify="center">
    <v-col cols="5" class = "my-6">
    <h2>2023年度  KDDIハッカソン学会  &nbsp; 会場:クサヤ温泉</h2>
    <v-card class="pa-2 my-6">
      <v-img :src="receivedImage" alt="WordCloud Image" v-if="receivedImage" />
    <v-card-title class="headline mb-0" style="white-space: pre-line;">
      音楽と感情に関する研究の展開
    </v-card-title>
    <v-card-subtitle class="subtitle-1">
      森数馬
    </v-card-subtitle>
    <v-card-text>
      キーワード：
      <br>
      音楽
      <br>
      音楽及び音響特徴
      <br>
      音楽パフォーマンス
      <br>
      時系列
      <br>
      心理生理学的反応
      <br>
      感情反応
    </v-card-text>
  </v-card>
    </v-col>
    <v-col cols="5">
      <ChatPage @imageData="handleImageData" />
    </v-col>
  </v-row>
</template>

<script>
import { defineComponent } from 'vue';
import ChatPage from '@/components/ChatPage.vue';

export default defineComponent({
  name: 'Chat6View',
  components: {
    ChatPage,
  },
  data() {
    return {
      receivedImage: "/images/music.png",
    };
  },
  mounted() {
  },
  methods: {
    handleImageData(imageBinary) {
      this.receivedImage = imageBinary;
    },
  }
}
);
</script>