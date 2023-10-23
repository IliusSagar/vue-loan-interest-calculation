<template>
  <div>
    <div style="margin: 50px auto; max-width: 700px;">
      <label><b>Enter Principle (BDT.): </b></label>
      <input type="text" class="form-control" v-model="principle"><br>

      <label><b>Enter Rate (% p.a.): </b></label>
      <input type="text" class="form-control" v-model="rate"><br>

      <label><b>Enter Time (yrs): </b></label>
      <input type="text" class="form-control" v-model="time"><br>

      <button @click="calculateSimpleInterest">Calculate</button>
    </div>
    <div>
      <p><b>Simple Interest: {{ simpleinterest }}</b></p>
    </div>

    <br><hr>
    <h6>Your results below</h6>
    <b>Principle: </b>{{principle}}<br>
    <b>Rate: </b>{{rate}}<br>
    <b>Time: </b>{{time}}<br>

  </div>
</template>

<script setup>
import { ref } from 'vue';

const principle = ref(0);
const rate = ref(0);
const time = ref(0);
const simpleinterest = ref(0);

function calculateSimpleInterest() {
  simpleinterest.value = (principle.value * rate.value * time.value) / 100;
}
</script>

<style scoped>

</style>
