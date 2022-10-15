<template>
    <div>
  <navbar />
  <section class="contact">

<h1 class="heading"> Remember Of <span>Day 6</span> </h1>
   
        <h1>My day</h1>

        <p>WE ARE MY DAY</p>

    <div class="content">
        <h3>hi, {{name}}</h3>
        <span>{{remember}}</span>
        <p>{{ค่าย}}</p>
    </div>

  
</section>
    </div>
</template>

         




<script>
import Navbar from '../components/Navbar.vue'
export default {
  components: { Navbar },
  data() {
      return {
        name: 'My Day',
        remember: 'เป็นวงดนตรีจากค่าย JYP Entertainment ปัจจุบันมีสมาชิกทั้งหมด 5 คน คือ เจ (🐥) , ซองจิน (🐻) , ยองเค (🦊) , วอนพิล (🐰) , โดอุน (🐶)',
        ค่าย: 'JYP Entertainment',
    }
  }
}  
</script>

<style>

</style>