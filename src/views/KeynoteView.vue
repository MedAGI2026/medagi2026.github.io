<template>
  <div id="keynote">
    <!-- Main Title -->
    <div class="main-title">
    	<h1>Keynote</h1>
		  <div class="main-title-deco"></div>
    </div>
    <!-- Main Title End -->

    <!-- Preliminary Keynotes -->
		<div id="keynotes">
			<!-- <h2>TBD</h2><hr> -->
			<div id="keynote-container">
        <div class="keynote-box">
					<div class="keynote-title">Hypergraph Computation for Medical Data</div>
          <div class="profile-box">
            <img src="@/assets/keynotes/Yue_Gao.jpg" class="profile" style="object-position: top;">
            <div class="">
              <div class="keynote-speaker">Dr Yue Gao</div>
              <div class="affiliation"><i>Tsinghua University, China</i></div>
            </div>
          </div>
          <div class="speaker-bio">
            <b>Abstract.</b> Structure data and related neural networks have attracted much attention in both research and industrial fields and become very hot topics in these years. It is noted that the world is far more complex than just pairwise connections. Hypergraph, as a generation of graph, is able to formulate such high-order correlations among the data and has been investigated in last decades. In this part, we first introduce the basic concepts and characteristics of hypergraphs. Next, focusing on hypergraph computation, we introduce hypergraph structural modelling, hypergraph structural evolution, and hypergraph neural network models. Finally, we introduce the application of hypergraph computation for medical data.
            <br><b>Bio.</b> Yue Gao is an associate professor in School of Software, Tsinghua University, Beijing, China. His research falls in the field of artificial intelligence and hypergraph learning. He leads the iMoon laboratory. He has large experience in developing hypergraph neural networks and complex interaction networks with a wide range of real-world applications including computer vision and medical image analysis.
          </div>
				</div>
				<div class="keynote-box">
					<div class="keynote-title">Smart Digital Health: From Foundation Model to Agentic AI to World Model</div>
          <div class="profile-box">
            <img src="@/assets/keynotes/Shujun_Wang.jpg" class="profile">
            <div>
              <div class="keynote-speaker">Dr Shunjun Wang</div>
              <div class="affiliation"><i>Hong Kong Polytechnic University, China</i></div>
            </div>
          </div>
          <div class="speaker-bio">
            <b>Abstract.</b> Artificial intelligence in medical imaging is moving from task-specific models toward systems that can perceive multimodal evidence, reason clinically, and forecast disease progression. Using Alzheimer’s disease as a case study, this talk presents a roadmap from foundation models to agentic AI and brain world models. First, multimodal foundation models address fragmented evidence through self-supervised and cross-modal pretraining, supporting downstream tasks despite missing modalities and long-tail combinations. Second, AD-CARE combines large language models, specialist tools, and guidelines to produce evidence-grounded, verifiable diagnostic reports. Evaluations across six datasets demonstrate improved accuracy, subgroup fairness, model compatibility, and clinician efficiency under incomplete real-world inputs. Finally, a generative brain world model represents disease progression as latent drift, enabling personalized forecasting of structural changes over time. Together, these advances suggest a path beyond static prediction toward deployable systems that integrate heterogeneous evidence, explain diagnostic reasoning, and simulate future patient trajectories for earlier intervention and individualized care.
            <br><b>Bio.</b> Dr. Shujun Wang is an Assistant Professor in the Department of Biomedical Engineering at The Hong Kong Polytechnic University and an affiliated member of the Department of Data Science and Artificial Intelligence. She received her PhD from The Chinese University of Hong Kong and previously conducted research at CUHK and the University of Cambridge. Her research focuses on artificial intelligence for digital health and smart ageing, with particular interests in multimodal foundation models, medical vision-language models, agentic AI, and brain world models for personalized diagnosis and prognosis. She has published more than 50 papers in leading journals and conferences, including Nature Communications, The Lancet Digital Health, IEEE Transactions on Medical Imaging, Medical Image Analysis, NeurIPS, ICML, and CVPR. Her research has received approximately 6,000 citations. She is also a recipient of Best Paper Awards at MICCAI workshops in 2022 and 2025.
          </div>
				</div>
			</div>
    </div>
    <!-- Preliminary Keynotes End -->
  </div>
</template>

<style scoped>
@media screen and (min-width: 1280px) {
  #keynote {
    width: 1280px;
    min-height: calc(100vh - 80px);
    margin: 0 calc(50vw - 640px);
    padding-bottom: 120px;
    padding-top: 80px;
    background-color: white;
  }

  .main-title {
    margin-top : 44px;
    margin-bottom: 40px;
  }

  h1 {
    font-family: Helvetica;
    margin: 0;
    font-size: 40px;
  }

  .main-title-deco {
    width: 28px;
    height: 1px;
    border: solid 2px #000000;
    background-color: #5b5b5b;
  }

  h2 {
    font-family: Helvetica;
    margin-bottom: 0px;
    font-family: Helvetica;
    font-size: 28px;
  }

  hr {
    border: 1px solid black;
  }

  /* Preliminary Keynote */
  #keynote-container {
    padding: 20px;
  }

  .keynote-box {
    margin-bottom: 50px;
  }

  .keynote-title {
    font-family: Helvetica;
    font-size: 32px;
    font-weight: bold;
    color: #000;
    padding-bottom: 10px;
  }

  .profile-box {
    display: flex;
    align-items: flex-end;
    margin: 10px 15px;
  }

  .profile {
    width: 100px;
    height: 100px;
    margin-right: 20px;
    border-radius: 50px;
    border: solid 1px #979797;
    object-fit: cover;
  }

  .keynote-speaker {
    font-family: Helvetica;
    font-size: 20px;
    font-weight: 300;
    color: #000;
    padding-bottom: 5px;
  }

  .affiliation {
    font-family: Helvetica;
    font-size: 14px;
    font-weight: 300;
    color: #797979;
    padding-bottom: 10px;
  }

  .speaker-bio {
    padding-left:10px;
    padding-top: 5px;
    padding-bottom: 10px;
    font-family: Helvetica;
    font-size: 18px;
    line-height: 1.4;
    color: #000;
  }
  /* Preliminary Keynote End */
}

@media screen and (min-width: 768px) and (max-width: 1279px) {
  #keynote {
    width: 720px;
    min-height: calc(100vh - 64px);
    margin: 0 calc(50vw - 360px);
    padding-bottom: 100px;
    padding-top: 64px;
    background-color: white;
  }

  .main-title {
    margin-top : 44px;
    margin-bottom: 30px;
  }

  h1 {
    font-family: Helvetica;
    margin: 0;
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

  /* Preliminary Keynote */
  #keynote-container {
    padding: 10px 0;
  }

  .keynote-box {
    margin-bottom: 30px;
  }

  .keynote-title {
    font-family: Helvetica;
    font-size: 28px;
    font-weight: bold;
    color: #000;
    padding-bottom: 10px;
  }


  .profile-box {
    display: flex;
    align-items: center;
    margin: 10px 0;
  }

  .profile {
    width: 100px;
    height: 100px;
    margin-right: 20px;
    border-radius: 50px;
    border: solid 1px #979797;
    object-fit: cover;
  }


  .keynote-speaker {
    font-family: Helvetica;
    font-size: 16px;
    font-weight: 300;
    color: #000;
    padding-bottom: 5px;
  }

  .affiliation {
    font-family: Helvetica;
    font-size: 14px;
    font-weight: 300;
    color: #797979;
  }

  .speaker-bio {
    padding-left:10px;
    padding-top: 10px;
    padding-bottom: 10px;
    font-family: Helvetica;
    font-size: 16px;
    line-height: 1.4;
    color: #000;
  }
  /* Preliminary Keynote End */
}

@media screen and (max-width: 767px) {
  #keynote {
    width: 360px;
    min-height: calc(100vh - 84px);
    margin: 0 calc(50vw - 180px);
    padding-top: 54px;
    padding-bottom: 30px;
  }

  .main-title {
    margin-top : 24px;
    margin-bottom: 30px;
  }

  h1 {
    font-family: Helvetica;
    margin: 0;
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
    font-size: 20px;
  }

  hr {
    border: 1px solid black;
  }

  /* Preliminary Keynote */
  #keynote-container {
    padding: 10px 0;
  }

  .keynote-box {
    margin-bottom: 30px;
  }

  .keynote-title {
    font-family: Helvetica;
    font-size: 20px;
    font-weight: bold;
    color: #000;
    padding-bottom: 5px;
  }

  .profile-box {
    display: flex;
    flex-direction: column;
    margin: 10px 0px;
  }

  .profile {
    width: 60px;
    height: 60px;
    margin-bottom: 10px;
    border-radius: 50px;
    border: solid 1px #979797;
    object-fit: cover;
  }


  .keynote-speaker {
    font-family: Helvetica;
    font-size: 16px;
    font-weight: 300;
    color: #000;
    padding-bottom: 5px;
  }

  .affiliation {
    font-family: Helvetica;
    font-size: 12px;
    font-weight: 300;
    color: #797979;
  }

  .speaker-bio {
    padding-left:10px;
    padding-bottom: 10px;
    font-family: Helvetica;
    font-size: 14px;
    line-height: 1.4;
    color: #000;
  }
  /* Preliminary Keynote End */
}
</style>

<script>
export default {
  computed: {
  currentYear() {
    return this.$route.params.year || new Date().getFullYear().toString();
    }
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
    }
  },
  created(){
    this.fetchData();
  },
}
</script>