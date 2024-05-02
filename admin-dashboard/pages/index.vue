<template>
  <div class="container">
    <div class="header">
      <h1>Dashboard</h1>
      <button>Settings</button>
    </div>
    <div class="card" v-for="(card, index) in cards" :key="index">
      <h2>{{ card.title }}</h2>
      <p>{{ card.content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Card 1',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor, magna a ullamcorper elementum, velit velit rhoncus nibh, ac auctor velit nisi vel sapien.'
        },
        {
          title: 'Card 2',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor, magna a ullamcorper elementum, velit velit rhoncus nibh, ac auctor velit nisi vel sapien.'
        },
        {
          title: 'Card 3',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor, magna a ullamcorper elementum, velit velit rhoncus nibh, ac auctor velit nisi vel sapien.'
        },
        {
          title: 'Card 4',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor, magna a ullamcorper elementum, velit velit rhoncus nibh, ac auctor velit nisi vel sapien.'
        }
      ]
    }
  }
}
</script>

<style>
.container {
  width: 80%;
  max-width: 800px;
  height: 80%;
  max-height: 800px;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: auto 1fr;
  gap: 20px;
  padding: 20px;
  overflow-y: auto;
}

.header {
  grid-column: 1/-1;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 50px;
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 10px;
  padding: 0 20px;
}

.header h1 {
  color: #fff;
  font-size: 24px;
}

.header button {
  background-color: transparent;
  border: none;
  color: #fff;
  font-size: 18px;
  cursor: pointer;
}

.card {
  grid-column: span 6;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.card h2 {
  color: #fff;
  font-size: 20px;
}

.card p {
  color: #fff;
  font-size: 16px;
}

.card:nth-child(even) {
  grid-column: span 6 start/span 6 end;
}
</style>