<template>
  <v-row justify="center">
    <v-col cols="5" class = "my-6">
    <h2>2023年度  KDDIハッカソン学会  &nbsp; 会場:クサヤ温泉</h2>
    <v-card class="pa-2 my-6">
      <v-img :src="receivedImage" alt="WordCloud Image" v-if="receivedImage" />
    <v-card-title class="headline mb-0" style="white-space: pre-line;">
      「戦後『新建築』誌に見られた建築家の創作の主題」に対する討論
    </v-card-title>
    <v-card-subtitle class="subtitle-1">
      奥山信一
    </v-card-subtitle>
    <v-card-text>
      キーワード：
      <br>
      戦後建築
      <br>
      新建築運動
      <br>
      建築史
      <br>
      創造性
      <br>
      建築デザイン
      <br>
      モダニズム
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
  name: 'Chat2View',
  components: {
    ChatPage,
  },
  data() {
    return {
      receivedImage: "/images/construction.png",
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