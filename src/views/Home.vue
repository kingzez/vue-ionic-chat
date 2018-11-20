<template>
  <div>
    <ion-header>
      <ion-toolbar color="dark">
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>ionic Chat</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-tabs>
      <!-- 聊天 -->
      <ion-tab tab="chat">
        <ion-list>
          <ion-list-header>
            <ion-label>placeholder</ion-label>
          </ion-list-header>
          <ion-item v-for="chatItem in chatItems" :key="chatItem.$index">
            <ion-avatar slot="start">
              <img :src="chatItem.avatar">
            </ion-avatar>
            <ion-label>
              <h2>{{ chatItem.name }}</h2>
              <h3>{{ chatItem.lastWord }}</h3>
              <p>{{ chatItem.msg }}</p>
            </ion-label>
          </ion-item>
        </ion-list>
      </ion-tab>

      <!-- 通讯录 -->
      <ion-tab tab="account">
        <ion-list>
          <ion-list-header>
            <ion-label>placeholder</ion-label>
          </ion-list-header>
        </ion-list>
        通讯录 Content
      </ion-tab>

      <!-- 发现 -->
      <ion-tab tab="discover">
        <ion-card>
          <ion-img src="https://avatars3.githubusercontent.com/u/10891613?s=460&v=4"></ion-img>
          <ion-card-header>
            <ion-card-title>Hello World</ion-card-title>
          </ion-card-header>
          <ion-card-content>
            <p>The content for this card</p>
          </ion-card-content>
        </ion-card>
      </ion-tab>

      <!-- 我 -->
      <ion-tab tab="me">
        <Me />
      </ion-tab>

      <!-- footer tab bar -->
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="chat">
          <ion-label>聊天</ion-label>
          <ion-icon name="chatbubbles"></ion-icon>
        </ion-tab-button>

        <ion-tab-button tab="account">
          <ion-label>通讯录</ion-label>
          <ion-icon name="contact"></ion-icon>
        </ion-tab-button>

        <ion-tab-button tab="discover">
          <ion-label>发现</ion-label>
          <ion-icon name="compass"></ion-icon>
        </ion-tab-button>

        <ion-tab-button tab="me">
          <ion-label>我</ion-label>
          <ion-icon name="person"></ion-icon>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </div>

</template>


<script>
// @ is an alias to /src
import Me from "./Me.vue";

export default {
  name: "home",
  data() {
    return {
      chatItems: [
        {
          name: "Finn",
          avatar: "https://avatars3.githubusercontent.com/u/10891613?s=460&v=4",
          lastWord: "I'm a big deal",
          msg: "Listen, I've had a pretty messed up day..."
        },
        {
          name: "Finn",
          avatar: "https://avatars2.githubusercontent.com/u/153183?s=460&v=4",
          lastWord: "I'm a big deal",
          msg: "Listen, I've had a pretty messed up day..."
        },
        {
          name: "Finn",
          avatar: "https://avatars3.githubusercontent.com/u/10891613?s=460&v=4",
          lastWord: "I'm a big deal",
          msg: "Listen, I've had a pretty messed up day..."
        },
        {
          name: "Finn",
          avatar: "https://avatars2.githubusercontent.com/u/153183?s=460&v=4",
          lastWord: "I'm a big deal",
          msg: "Listen, I've had a pretty messed up day..."
        }
      ]
    };
  },
  components: {
    Me
  }
};
</script>
<style>
</style>
