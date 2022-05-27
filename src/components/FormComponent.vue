<template>
  <div>
    <form>
      <input type="text" placeholder="Name"><hr>
      <input type="email" placeholder="E-Mail"><hr>
      <input type="number" placeholder="Idade"><hr>
      <input type="radio" name="sex" value="M"> Male
      <span>|</span>
      <input type="radio" name="sex" value="F"> Female
     <hr>
      <select>
        <option value="">select city</option>
        <option value="lb">Lisbon</option>
        <option value="pt">Porto</option>
        <option value="av">Aveiro</option>
        <option value="vi">Viseu</option>
      </select>
      <hr>
      <label for="agree">I agree with the terms of use</label>
      <input type="checkbox" id="agree">
      <hr>
      <textarea cols="30" rows="10"></textarea>
      <hr>
      <button typ="submit">Send</button>
    </form>
  </div>
</template>

<script>

export default {
  data(){
    return{
      msg: "Hi"
    }
  }
}

</script>

