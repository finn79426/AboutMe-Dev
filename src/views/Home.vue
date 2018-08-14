<template>
  <div class="card-container">
    <div id="head" class="card card-head">
      <div class="image" :style="{ 'background-image': `url(${photo})` }"></div>
      <div class="content">
        <h1>{{ name }}</h1>
        <p>{{ id }}</p>
      </div>
    </div>
    <div id="link" class="icon-list">
      <div class="icon" v-for="(contact, i) in contacts" :key="i">
        <a :href="contact.link" target="_blank"><font-awesome-icon :icon="contact.icon" /></a>
      </div>
    </div>
    <div id="about" class="card">
      <h2>關於我</h2>
      <p>解決小問題，沒有大問題</p>
      <p>我是曹富翔，大家都叫我小曹，我喜歡用程式語言解決日常所遇到的問題來改善生活</p>
      <p>專長在資安，現任 6l0ry CTF Team 與 TDOHacker 漏洞挖掘小組</p>
    </div>
    <div id="skill" class="card">
      <h2>技能樹</h2>
      <div class="rate" v-for="(item, i) in skill" :key="i">
        <p>{{ item.name }}</p>
        <div class="bar" :class="`rate-${item.rate}`"></div>
      </div>
    </div>
    <div id="experience" class="card">
      <h2>經驗</h2>
      <div v-for="(item, i) in experience" :key="i">
        <p class="tag">{{ item.date }}</p>
        <p>{{ item.title }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      name: '小曹',
      id: '@howpwn',
      photo: 'https://i.imgur.com/7WB99TK.jpg',
      contacts: [
        {
          link: 'https://github.com/finn79426',
          icon: ['fab', 'github']
        },
        {
          link: 'mailto:finn79426@gmail.com',
          icon: ['fas', 'envelope']
        },
        {
          link: 'tel:+886910950759',
          icon: ['fas', 'phone']
        },
        {
          link: 'https://fb.com/howpwn',
          icon: ['fab', 'facebook-f']
        },
        {
          link: 'http://blog.howpwn.tw',
          icon: ['fas', 'rss']
        },
        {
          link: 'https://t.me/h0wpwn',
          icon: ['fab', 'telegram-plane']
        }
      ],
      skill: [
        {
          name: 'Python',
          rate: 5
        },
        {
          name: 'Markdown',
          rate: 5
        },
        {
          name: 'Shell Script',
          rate: 4
        },
        {
          name: 'C',
          rate: 3
        },
        {
          name: 'Assembly',
          rate: 3
        },
        {
          name: 'HTML',
          rate: 3
        }
      ],
      experience: [
        {
          title: '6l0ry CTF Team',
          date: '現任'
        },
        {
          title: 'TDOHacker 漏洞挖掘研究組',
          date: '現任'
        },
        {
          title: '欣亞數位 - 組裝工讀生',
          date: '2016/04 - 2016/09'
        }
      ]
    }
  }
}
</script>
