<template>
  <div>
    <navbar />
    <section class="about">
      <h1 class="heading">about <span>Music</span></h1>

      <div class="row">
        <div class="info-container">
          <h1>personal info</h1>

          <div class="box-container">
            <div class="box">
              <h3><span>pop : </span> {{ pop }}</h3>
              <h3><span>rock : </span> {{ rock }}</h3>
              <h3><span>jazz : </span> {{ jazz }}</h3>
              <h3><span>country : </span> {{ country }}</h3>
            </div>

            <div class="box">
              <h3><span>type-pop : </span> มีความเป็นวัยรุ้นและเหมาะกับคนรักสบายๆชิลๆ</h3>
              <h3><span>type-rock : </span> ดุดันและชอบลุย</h3>
              <h3><span>type-jazz : </span> เป็นฟิลชอบอ่านหนังสือและหลิ่นไอแบบผู้ดี</h3>
              <h3><span>type-country : </span> ชิลๆบ้านๆเหมาะในงานฉลองปาร์ตี้</h3>
            </div>
          </div>

          <a href="/profilewithcss/files/resume.pdf" class="btn">
            download CV <i class="fas fa-download"></i>
          </a>
        </div>

        <div class="count-container">
          <div class="box">
            <h3>POP</h3>
            <p>EASY AND JOIN WITH FRIEND</p>
          </div>

          <div class="box">
            <h3>ROCK</h3>
            <p>BAND AND CONCERT</p>
          </div>

          <div class="box">
            <h3>JAZZ</h3>
            <p>CAFE , READING BOOK AND DATE</p>
          </div>

          <div class="box">
            <h3>COUNTRY</h3>
            <p>PARTY JOIN WITH FRIEND AND FEEL COUNTRY SIDE</p>
          </div>
        </div>
      </div>
    </section>

    <!-- about section ends -->

    <!-- skills section starts  -->

    <section class="skills">
      <h1 class="heading"><span>WHAT TYPE OF MUSIC</span> DO YOU LIKE ?</h1>

      
    </section>
    <!-- about section ends -->
  </div>
</template>
<script>
import Navbar from "../components/Navbar.vue";
import axios from "axios";

export default {
  components: { Navbar },
  methods: {
    async FetchExperience() {
      try {
        let res = await axios.get(
          "https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/experiences"
        );
        this.experiences = res.data;
      } catch (error) {}
    },
    async fetchskill() {
      try {
        let res = await axios.get(
          "https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/skills"
        );
        this.skill = res.data;
      } catch (error) {}
    },
  },
  data() {
    return {
      pop: "ฟังสบายๆและไม่เร็สไม่ช้า",
      rock: "ดุดันและมัน",
      jazz: "ฟังสยายๆแต่โน๊ตมีความซ้อน",
      country: "ชิลๆฟังสบายๆแต่มีกลิ่นไอแบบปอปผสมแจ๊ส",
      experiences: [],
      skill: [],
    };
  },
  beforeMount() {
    this.FetchExperience();
    this.fetchskill();
  },
};
</script>

<style>
</style>