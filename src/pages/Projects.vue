<template>
    <div>
        <navbar />
         <section class="projects">
        <h1 class="heading"> <span>Day 6</span> History </h1>
        <h3>{{name}}</h3>
        <p>{{detail}}</p>
        <p>{{song}}</p>
        <div class="box-container">
            <iframe width="720" height="405" src="https://www.youtube.com/watch?v=x3sFsHrUyLQ"
                title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; 
            gyroscope; picture-in-picture" allowfullscreen></iframe>
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
        name: 'Day 6 History',
        detail: 'เดย์ซิกซ์ (เกาหลี: 데이식스; อาร์อาร์: De-i-sik-seu) เป็นวงดนตรีป๊อปร็อคของเกาหลีใต้ภายใต้สังกัดเจวายพีเอนเตอร์เทนเมนต์ เปิดตัวเมื่อวันที่ 7 กันยายน พ.ศ. 2558 โดยมีอีพี เดอะเดย์ ซึ่งขึ้นถึงอันดับ 2 ในชาร์ตอัลบั้มโลกของบิลบอร์ด หนึ่งสัปดาห์หลังจากการเปิดตัว[1] วงดนตรีประกอบด้วยสมาชิกสี่คนได้แก่ ซ็องจิน, ย็องเค, ว็อนพิล และ โดอุน ซึ่งเดิมเป็นวงดนตรีหกคน โดยจุนฮย็อก (คีย์บอร์ด) ได้ออกจากวงไปในเดือนกุมภาพันธ์ พ.ศ. 2559[2] และเจ ได้ออกจากค่ายเมื่อวันที่ 31 ธันวาคม พ.ศ. 2564 ซึ่งสมาชิกเดย์ซิกซ์ทุกคนมีส่วนสำคัญในการเขียน, แต่งเพลง และผลิตเพลงของวง',
        song: 'เพลงเดบิวต์ เพลงแรก "Congratulations"' 
        }
    }
}    
</script>

<style>

</style>