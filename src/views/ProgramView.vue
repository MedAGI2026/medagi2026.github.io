<template>
    <div id="program">
      <!-- <h2>🔥🌟 To access the MedAGI 2025 proceedings, please visit  
          <a href="https://link.springer.com/book/10.1007/978-3-032-07845-2" target="_blank"> this link</a>. 🌟🔥
        </h2> -->
      <!-- Main Title -->
      <div class="main-title">
          <h1>Program</h1>
          <div class="main-title-deco"></div>
      </div>
      <!-- Main Title End -->
      <!-- <span id="thankyou"> -->
        
        <!-- </span> -->
       <!-- Program Schedules -->
      <div id="schedule">
        <!-- <h2>TBD</h2> -->
        <h2>Schedule</h2><hr>
        <table class="table">
          <tr>
            <td class="schedule-time">8:00 - 8:10</td>
            <td class="schedule-name">Opening Remarks</td>
          </tr>
          <tr>
            <td class="schedule-time">8:10 - 8:40</td>
            <td class="schedule-name">
              Keynote 1 <!-- : Prof. Jing Ke, Shanghai Jiao Tong University
              <span class="oral-authors">Why Human Clinical Expertise Remains Indispensable in AI Pathology Image Interpretation</span> -->
            </td>
          </tr>
          <tr>
            <td class="schedule-time">8:40 - 9:25</td>
            <td class="schedule-name">Oral Session 1</td>
          </tr>
          <tr>
            <td class="schedule-time">9:25 - 10:55</td>
            <td class="schedule-name">Poster Session  / Coffee Break (10:00 - 10:30)</td>
          </tr>
          
          <tr>
            <td class="schedule-time">10:55 - 11:25</td>
            <td class="schedule-name">
              Keynote 2 <!-- : Prof. Jaewoo Kang, Korea University / AIGEN Sciences Inc. 
              <span class="oral-authors">AI-driven Drug Discovery in the LLM Era</span> -->
            </td>
          </tr>
          <tr>
            <td class="schedule-time">11:25 - 12:10</td>
            <td class="schedule-name">Oral Session 2</td>
          </tr>
          <tr>
            <td class="schedule-time">12:10 - 12:20</td>
            <td class="schedule-name">Transition / Buffer</td>
          </tr>
          <tr>
            <td class="schedule-time">12:20 - 12:30</td>
            <td class="schedule-name">Closing / Awards</td>
          </tr>
        </table>
      </div>

      <!-- Oral Sessions -->
      <div id="oral">
        <h2>Oral Sessions</h2><hr>
        <table class="table">
          <tr v-for="(item, index) in oral1" :key="index">
            <td v-if="index === 0" :rowspan="oral1.length" class="oral-time">Oral 1<br>(8:40 - 9:25)</td>
              <td class="oral-content">
                [{{item['id']}}] {{item['name']}}
                [<a target="_blank" type="application/pdf" :href="`https://nbviewer.org/github/MedAGI2026/medagi2026.github.io/blob/main/src/assets/papers/${item['id']}.pdf`">paper</a>]
                <span v-if="item['posters']===true">
                  [<a target="_blank" type="application/pdf" :href="`https://github.com/MedAGI2026/medagi2026.github.io/blob/main/src/assets/posters/${item['id']}.pdf`">poster</a>]
                </span> 
                <span class="oral-authors" v-html="item['authors']"></span>
                
              </td>
          </tr>
          <tr v-for="(item, index) in oral2" :key="index">
              <td v-if="index === 0" :rowspan="oral2.length" class="oral-time">Oral 2<br>(11:25 - 12:10)</td>
              <td class="oral-content">
                [{{item['id']}}] {{item['name']}}
                [<a target="_blank" type="application/pdf" :href="`https://nbviewer.org/github/MedAGI2026/medagi2026.github.io/blob/main/src/assets/papers/${item['id']}.pdf`">paper</a>]
                <span v-if="item['posters']===true">
                  [<a target="_blank" type="application/pdf" :href="`https://github.com/MedAGI2026/medagi2026.github.io/blob/main/src/assets/posters/${item['id']}.pdf`">poster</a>]
                </span> 
                <span class="oral-authors" v-html="item['authors']"></span>
                
              </td>
          </tr>
        </table>

        
      </div>
      <!-- Oral Sessions End -->


      <div id="poster">
        <h2>Poster Sessions (9:25 - 10:55)</h2><hr>
        <table class="table">
          <tr>
            <td colspan="2" class="poster-title sticky-header">Full-length Papers</td>
          </tr>
          <tr v-for="(item, index) in paper" :key="index">
            <td class="poster-id">{{item['id']}} </td>
            <td class="poster-name">
              {{item['name']}} 
              [<a target="_blank" type="application/pdf" :href="`https://nbviewer.org/github/MedAGI2026/medagi2026.github.io/blob/main/src/assets/papers/${item['id']}.pdf`">paper</a>]
               <span v-if="item['posters']===true">
                [<a target="_blank" type="application/pdf" :href="`https://github.com/MedAGI2026/medagi2026.github.io/blob/main/src/assets/posters/${item['id']}.pdf`">poster</a>]
              </span> 
              
              <span class="oral-authors">{{ item['authors'] }}</span></td>
          </tr>
        </table>
        
        <table class="table">
          <tr>
            <td colspan="2" class="poster-title sticky-header">Extended Abstracts</td>
          </tr>
          
          <tr v-for="(item, index) in abstract" :key="index">
            <td class="oral-content">{{item['id']}}</td>
            <td class="oral-content">{{item['name']}}
              [<a target="_blank" type="application/pdf" :href="`https://nbviewer.org/github/MedAGI2026/medagi2026.github.io/blob/main/src/assets/papers/${item['id']}.pdf`">paper</a>]
              <span v-if="item['posters']===true">
                [<a target="_blank" type="application/pdf" :href="`https://github.com/MedAGI2026/medagi2026.github.io/blob/main/src/assets/posters/${item['id']}.pdf`">poster</a>]
              </span>
              <span class="oral-authors">{{ item['authors'] }}</span></td>
          </tr>
        </table>
      </div>
    </div>
  </template>
  
  <style scoped>
  @media screen and (min-width: 1280px) {
    #program {
      width: 1280px;
      min-height: calc(100vh - 80px);
      padding-left: calc(50vw - 640px);
      padding-right: calc(50vw - 640px);
      padding-top: 80px;
      background-color: white;
    }

    .main-title {
      margin-top: 44px;
      margin-bottom: 40px;
    }

    h1 {
      font-family: Helvetica;
      margin-bottom: 0;
      font-size: 40px;
    }

    .main-title-deco {
      width: 28px;
      height: 1px;
      border: solid 2px #000000;
      background-color: #5b5b5b;
    }

    h2 {
      margin-bottom: 0px;
      font-family: Helvetica;
      font-size: 28px;
    }

    hr {
      border: 1px solid black;
    }

    .table {
      width: 100%;
      margin: 0;
      border-right:none; 
      border-left:none;
      border-bottom:none;
    }

    .table .no-border td {
      border: none !important;
      border-bottom: none !important;
      border-right: none !important;
    }

    table, th, td {
      border: 1px solid black;
      border-collapse: collapse;
      font-family: Helvetica;
    }

    .schedule-time {
      padding: 10px;
      width: 150px;
    }

    .schedule-name {
      padding: 10px;
    }

    /* Oral */
    #oral {
      margin-bottom: 40px;
    }

    #oral-table-m {
      display: none;
    }
    .oral-time {
      text-align: center;
      width: 200px;
    }

    .oral-content {
      padding: 15px;
      font-family: Helvetica;
      font-size: 14px;
    }

    .oral-authors {
      display: block;
      margin-top: 5px;
      font-family: Helvetica;
      font-style: italic;
      color: #9b9b9b;
      font-size: 12px;
    }
    
    /* Oral end */

    /* Poster */
    #poster {
      margin-bottom: 40px;
    }

    #poster > table {
      margin-bottom: 20px;
    }

    .poster-title {
      padding: 15px;
      font-size: 22px;
      font-weight: bold;
      text-align: center!important;
    }

    .poster-id {
      padding: 15px;
      text-align: center;
      width: 50px;
    }

    .poster-name {
      padding: 15px;
    }
    /* Poster end */
  }
  
  @media screen and (min-width: 768px) and (max-width: 1279px) {
    #program {
      width: 720px;
      min-height: calc(100vh - 64px);
      padding-left: calc(50vw - 360px);
      padding-right: calc(50vw - 360px);
      padding-top: 64px;
      background-color: white;
    }

    .main-title {
      margin-top: 44px;
      margin-bottom: 30px;
    }

    h1 {
      font-family: Helvetica;
      margin-bottom: 0;
      font-size: 36px;
    }

    .main-title-deco {
      width: 28px;
      height: 1px;
      border: solid 2px #000000;
      background-color: #5b5b5b;
    }

    h2 {
      margin-bottom: 0px;
      font-family: Helvetica;
      font-size: 28px;
    }

    hr {
      border: 1px solid black;
    }

    .table {
      width: 100%;
      margin: 0;
      border-right:none; 
      border-left:none;
      border-bottom:none;
    }

    .table .no-border td {
      border: none !important;
      border-bottom: none !important;
      border-right: none !important;
    }

    table, th, td {
      border: 1px solid black;
      border-collapse: collapse;
      font-family: Helvetica;
    }

    .schedule-time {
      padding: 10px;
      width: 100px;
    }

    .schedule-name {
      padding: 10px;
    }

    /* Oral */
    #oral {
      margin-bottom: 40px;
    }

    #oral-table-m {
      display: none;
    }

    .oral-time {
      width: 120px;
      text-align: center;
      font-size: 16px;
    }

    .oral-content {
      padding: 15px;
      font-family: Helvetica;
      font-size: 14px;
    }
    .oral-authors {
      display: block;
      margin-top: 5px;
      font-family: Helvetica;
      font-style: italic;
      color: #9b9b9b;
      font-size: 12px;
    }
    
    /* Oral end */

    /* Poster */
    #poster {
      margin-bottom: 40px;
    }

    #poster > table {
      margin-bottom: 20px;
    }

    .poster-title {
      padding: 10px;
      font-size: 18px;
      font-weight: bold;
      text-align: center;
    }

    .poster-id {
      padding: 15px;
      text-align: center;
      font-family: Helvetica;
      font-size: 14px;
    }

    .poster-name {
      padding: 15px;
      font-family: Helvetica;
      font-size: 14px;
    }
    /* Poster end */

  }

  @media screen and (max-width: 767px) {
    #program {
      width: 360px;
      min-height: calc(100vh - 30px);
      padding-left: calc(50vw - 180px);
      padding-right: calc(50vw - 180px);
      padding-top: 54px;
      padding-bottom: 30px;
      background-color: white;
    }

    .main-title {
      margin-top: 24px;
      margin-bottom: 30px;
    }

    h1 {
      font-family: Helvetica;
      margin-bottom: 0;
      font-size: 24px;
    }

    .main-title-deco {
      width: 20px;
      height: 1px;
      border: solid 2px #000000;
      background-color: #5b5b5b;
    }

    h2 {
      margin-bottom: 0px;
      font-family: Helvetica;
      font-size: 28px;
    }

    hr {
      border: 1px solid black;
    }

    .table {
      width: 100%;
      margin: 0;
      border-right:none; 
      border-left:none;
      border-bottom:none;
    }

    .table .no-border td {
      border: none !important;
      border-bottom: none !important;
      border-right: none !important;
    }

    table, th, td {
      border: 1px solid black;
      border-collapse: collapse;
      font-family: Helvetica;
    }
    
    .schedule-time {
      font-size: 14px;
      padding: 10px;
      width: 100px;
    }

    .schedule-name {
      font-size: 14px;
      padding: 10px;
    }

    .sticky-header {
      position: sticky;
      top: 64px;
      background-color: lightgray;
    }

    /* Oral */
    #oral {
      margin-bottom: 40px;
    }

    #oral-table {
      display: none;
    }
    .oral-time-m {
      text-align: center;
      font-size: 16px;
      font-weight: bold;
      padding: 10px;
    }

    .oral-content {
      padding: 15px;
      font-size: 14px;
    }

    .oral-authors {
      display: block;
      margin-top: 5px;
      font-family: Helvetica;
      font-style: italic;
      color: #9b9b9b;
      font-size: 12px;
    }
    
    /* Oral end */

    /* Poster */
    #poster {
      margin-bottom: 40px;
    }

    #poster > table {
      margin-bottom: 20px;
    }

    .poster-title {
      text-align: center;
      font-size: 16px;
      font-weight: bold;
      padding: 10px;
    }

    .poster-id {
      padding: 15px;
      text-align: center;
      font-size: 14px;
    }

    .poster-name {
      padding: 15px;
      font-size: 14px;
    }
    /* Poster end */

  }
  </style>
  
<script>
import program from "@/assets/info/program_2026.json";

export default {
  computed: {
  currentYear() {
    return this.$route.params.year || new Date().getFullYear().toString();
    }
  },

  data() {
    return {
      oral1 : program[0]['oral1'],
      oral2 : program[0]['oral2'],
      paper : program[0]['full_length'],
      abstract : program[0]['abstract'],
    }
  },
  mounted() {
    console.log('paper:', this.paper);
  },
  methods: {
      fetchData() {
      // Use the currentYear computed property to determine which data to fetch
      const year = this.currentYear;
      if (year === '2023') {
        // Fetch and set the data for the 2023 archive
      } else {
        // Fetch and set the data for the current year
      }
    },

    // getPaperUrl(id) {
    //   return require(`@/assets/papers/${id}.pdf`).default;
    // }
  },
  created(){
    this.fetchData();
  },
}
</script>