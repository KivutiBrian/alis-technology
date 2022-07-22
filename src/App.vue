<script setup lang="ts">
import { ref } from 'vue';

const date = ref("")
const email = ref("")

// send email
const sendEmail = (): void => {

  // include api call to send email to user

  alert(`Congratulations, you have selected ${date.value}`)
  date.value = ""
  email.value = ""

}
</script>

<template>
  <div>
    <form class="main">
      <!-- datepicker -->
      <div class="form-group">
        <label for="">Select a date</label>
        <input v-model="date" type="date" required>
      </div>
      <!-- input -->
      <div class="form-group">
        <label for="">Email Address</label>
        <input v-model="email" type="text" required>
      </div>
      <!-- submit button -->
      <div class="form-group">
        <button @click.prevent="sendEmail" class="submit">Submit</button>
      </div>
    </form>
  </div>

</template>

<style scoped lang="scss">
.main {

  box-sizing: border-box;
  padding: 2rem;
  border-radius: 1rem;
  background-color: hsl(0, 0%, 100%);
  border: 4px solid hsl(0, 0%, 90%);
  display: grid;

}

input {
  padding: 0.5rem;
  width: 100%;
  border: 1px solid;
}

.form-group {
  display: flex;
  flex-direction: column;
  margin: 20px 0;
  width: 100%;
}

.submit {
  padding: 0.5rem;
  font-size: 1rem;
  font-family: 'Times New Roman', Times, serif;
}

.submit:hover {
  cursor: pointer;
  background-color: bisque;
}
</style>
