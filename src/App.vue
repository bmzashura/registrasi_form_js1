<script setup>
import { ref } from 'vue'

const firstName = ref('')
const lastName = ref('')

function submitForm() {
  console.log(`Nama Lengkap : ${firstName.value} ${lastName.value}`)
}
</script>

<template>
  <main class="container">
    <h1>Form Registrasi</h1>

    <form @submit.prevent="submitForm" class="form">
      <div class="field">
        <label for="first">Nama Depan</label>
        <input id="first" v-model="firstName" type="text" placeholder="Masukkan nama depan" />
      </div>

      <div class="field">
        <label for="last">Nama Belakang</label>
        <input id="last" v-model="lastName" type="text" placeholder="Masukkan nama belakang" />
      </div>

      <button type="submit" class="btn">Kirim</button>
    </form>
  </main>
</template>

<style scoped>
.container {
  max-width: 480px;
  margin: 48px auto;
  padding: 24px;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  font-family:
    system-ui,
    -apple-system,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial;
}
.form {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.field {
  display: flex;
  flex-direction: column;
}
.field label {
  font-size: 14px;
  margin-bottom: 6px;
}
.field input {
  padding: 8px 10px;
  border: 1px solid #cbd5e1;
  border-radius: 4px;
}
.btn {
  padding: 10px 12px;
  background: #2563eb;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
.btn:hover {
  background: #1d4ed8;
}
</style>
