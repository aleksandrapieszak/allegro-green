<template>
    <div class="container">
      <!-- <button @click="incrementCount" class="btn">
        Kliknięto: {{ count }}
      </button>
  
      <button @click="toggleUsers" class="btn">
        Pokaż/Ukrzyj Użytkowników
      </button>
  
      <ul v-if="showUsers" class="user-list">
        <li>Szymon</li>
        <li>Ola</li>
        <li>Mariusz</li>
      </ul> -->
  
      <label class="checkbox-label">
        <input type="checkbox" @click="toggleTextVisibility" />
        Ukryj tekst
      </label>
  
      <p v-if="isTextVisible" class="text-block">
        Przykładowy tekst
      </p>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { ref } from 'vue'
  
  const count = ref(0)
  const showUsers = ref(false)
  const isTextVisible = ref(true)
  
  const incrementCount = () => {
    count.value++
  }
  
  const toggleUsers = () => {
    showUsers.value = !showUsers.value
  }
  
  const toggleTextVisibility = () => {
    isTextVisible.value = !isTextVisible.value
  }
  </script>
  
  <style scoped>
  .container {
    padding: 1rem;
    font-family: sans-serif;
  }
  
  .btn {
    display: inline-block;
    margin: 0.5rem 1rem;
    padding: 0.5rem 1rem ;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .user-list {
    margin: 0.5rem 0;
    padding-left: 1.5rem;
  }
  
  .checkbox-label {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin: 0.5rem 0;
  }
  
  .text-block {
    margin-top: 1rem;
    color: #333;
  }
  </style>
  