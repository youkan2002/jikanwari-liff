<template>
  <v-container column justify-center align-center>
    <v-row class="text-center">
      <v-col>
        <h2>LINEで時間割を管理しよう</h2>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col>
        <p>
          時間割表、なくしますよね？
          <br />時間割表、覚えたくないですよね？
          <br />明日が何曜日かすぐにわかりますか？
          <br />
          <br />1つでも当てはまったそこのあなた
          <br />すべてLINEで管理しませんか？
        </p>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="text-center video">
        <video src="~static/video/top.mp4" autoplay loop style="max-width: 100%" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="0" md="4" />
      <v-col md="2" class="text-center">
        <p>LINEで使う</p>
        <a href="https://line.me/R/ti/p/%40ywg0561x">
          <img
            width="140"
            height="43"
            border="0"
            alt="友だち追加"
            src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png"
          />
        </a>
      </v-col>
      <v-col md="2" class="text-center">
        <p>Webで使う</p>
        <v-btn nuxt to="/table" color="primary" x-large height="43" width="140">Web</v-btn>
      </v-col>
      <v-col cols="0" md="4" />
    </v-row>
  </v-container>
</template>

<script>

export default {
  components: {
  },
  mounted() {
    this.$store.state.jikanwari = '';
    this.$store.commit('updateLoading', false);
  }
};
</script>

<style scoped>
v-btn {
  font-size: 30px;
}

@media screen and (max-width: 992px) {
  video {
    height: 300px;
  }
}
@media screen and (min-width: 992px) {
  video {
    height: 500px;
  }
}
body {
  background-color: #1976d2;
}
</style>
