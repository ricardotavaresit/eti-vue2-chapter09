<template>
  <div>
    <form>
      <input type="text" placeholder="Name" v-model="userData.name"> {{userData.name}} <hr>
      <input type="email" placeholder="E-Mail" v-model="userData.email"><hr>
      <input type="number" placeholder="Idade" v-model.number="userData.age"><hr>
      <input type="radio" name="sex" value="M" v-model="userData.sex"> Male
      <span>|</span>
      <input type="radio" name="sex" value="F" v-model="userData.sex"> Female
      {{userData.sex}}
     <hr>
      <select v-model="userData.state">
        <option value="">select city</option>
        <option value="lb">Lisbon</option>
        <option value="pt">Porto</option>
        <option value="av">Aveiro</option>
        <option value="vi">Viseu</option>
      </select>
      <p v-if="userData.state">select City: {{userData.state}}</p>
      <hr>
      <label for="agree">I agree with the terms of use</label>
      <input type="checkbox" id="agree" v-model="userData.terms">
      <hr>
      <textarea cols="30" rows="10" v-model="userData.description"></textarea>
      <hr>
      <button typ="submit">Send</button>
    </form>
  </div>
</template>

<script>

export default {
  data(){
    return{
      userData:{
        name:'',
        email:'',
        age:'',
        sex:'',
        state:'',
      },
      terms: true,
      description:''
    }
  }
}

</script>

