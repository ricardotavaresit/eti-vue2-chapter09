<template>
  <div>
    <form>
      <input type="text" placeholder="Name" v-model="userData.name" />
      {{ userData.name }}
      <hr />
      <input
        type="email"
        name="email"
        v-validate="'required|email'"
        placeholder="E-Mail"
        v-model="userData.email"
      />

     <!--  <div v-bind:class="{ 'is-danger': errors.has('email') }"> -->
      <div v-bind:class=" errors.has('email') ?  'is-danger' : 'is-success'">
        <span v-show="errors.has('email')" class="help is-danger">{{
          errors.first("email")
        }}</span>
      </div>
      <hr />
      <input type="number" placeholder="Idade" v-model.number="userData.age" />
      <hr />
      <input type="radio" name="sex" value="M" v-model="userData.sex" /> Male
      <span>|</span>
      <input type="radio" name="sex" value="F" v-model="userData.sex" /> Female
      {{ userData.sex }}
      <hr />
      <select v-model="userData.state">
        <option value="">select city</option>
        <option value="lb">Lisbon</option>
        <option value="pt">Porto</option>
        <option value="av">Aveiro</option>
        <option value="vi">Viseu</option>
      </select>
      <p v-if="userData.state">select City: {{ userData.state }}</p>
      <hr />
      <label for="agree">I agree with the terms of use</label>
      <input type="checkbox" id="agree" v-model="userData.terms" />
      <hr />
      <textarea cols="30" rows="10" v-model="userData.description"></textarea>
      <p>Version 1</p>
      <div class="text-formate">
        {{ userData.description }}
      </div>
      <p>Version 2</p>
      <pre>
        {{ userData.description }}
      </pre>
      <hr />
      <button typ="submit">Send</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {
        name: "",
        email: "",
        age: "",
        sex: "",
        state: "",
      },
      terms: true,
      description: "",
    };
  },
};
</script>


  <style scoped>
  .text-formate {
    white-space: pre;
  }

  .is-danger {
    border: 1px solid rgb(179, 11, 11);
  }
  .is-danger p {
    color: rgb(179, 11, 11);
  }


  .is-success {
    border: 1px solid rgb(12, 123, 27);
  }
  .is-success p {
    color: rgb(12, 123, 27);
  }

</style>
