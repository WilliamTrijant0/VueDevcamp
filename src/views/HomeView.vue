<script setup>
// export default {
//   data() {
//     return {
//       count: 0
//     }
//   }
// }
import { ref, computed } from 'vue';
// import TheWelcome from '../components/TheWelcome.vue'
// const msg = 'Halo bang'
// const deadline = ref('2023-05-26');
// const hariIni = ref('2023-06-03')
// const selesai = ref(true);

// const isDeadlineToday = computed(() => {
//   return deadline.value === hariIni;
// });

// const isTaskCompleted = computed(() => {
//   return selesai.value;
// });

const awesome = ref(true);

const count = ref(0);

// Fungsi untuk menangani klik tombol
const handleClick = () => {
  count.value++;
};

const items = ref([
      { id: 1, name: "Bawang", price: 1000 },
      { id: 2, name: "Semongko", price: 2000 },
      { id: 3, name: "Lombok", price: 3000 },
    ]);

// export default{}

</script>

<template>
  <main>
  <button @click="awesome = !awesome" class="border">Toggle</button>

  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>

  <div>
    <button @click="handleClick" class="border-solid border-2 border-sky-500">Klik Saya</button>
    <p>Anda telah mengklik saya sebanyak {{ count }} kali.</p>
  </div>
  
  <div>
    <h1>List Rendering - Data Blonjoan</h1>
    <ul>
      <li v-for="item in items" :key="item.id">
        {{ item.name }} - {{ item.price }}
      </li>
    </ul>
  </div>
  


  </main>
</template>
