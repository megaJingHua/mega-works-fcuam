<template>
  <div>
    <Header title="特色" />
    <div class="container">
      <el-row :gutter="10" class="ma-0 pa-0" style="align-items: stretch">
        <el-col type="flex" :span="12" :xs="24" v-for="(item, i) in characteristicData" :key="i" class="pb-2">
          <el-card :body-style="{ padding: '0px' }">
            <img :src="item.img" />
            <div style="padding: 16px">
              <h5>{{ item.title }}</h5>
              <p v-html="item.context"></p>
            </div>
          </el-card>
        </el-col>
      </el-row>
    </div>
  </div>
</template>
<script>
import Header from "@/components/Header";
export default {
  components: { Header },
  data() {
    return {
      characteristicData: [
        {
          title: "多元化課程與學程",
          img: "http://www.math.fcu.edu.tw/2021_new_website/data/img/Characteristic1.jpg",
          context:
            "近年來資訊與網路快速的發展，應用數學結合資訊科學已是必然趨勢，本系因應這趨勢，開設多元化課程與學程，課程橫跨分析、微方、力學、統計、應用代數、離散數學、資訊軟體應用、精算、電腦網路應用、計算科學等領域。數學為應用科學的根本，因此本系積極開發相關教學網站，提供師生良好的網路學習環境，協助學生排除學習困境，提昇學習成效，以建立良好的數學基礎，為增進職場競爭力提供的最佳途徑。",
        },
        {
          title: "優質教學與跨領域研究",
          img: "http://www.math.fcu.edu.tw/2021_new_website/data/img/Characteristic2.jpg",
          context:
            "本系以優質教學與跨領域研究為主軸，禮聘優秀師資，整合教學與研究的資源，架構數位學習平台，並支援全校微積分的教學；開設就業相關學程，強調特色化、證照化與專業化，鼓勵學生學習第二專長，輔導協助學生就業。提供多元化教學資源，培育優質數學種子及未來高科技人才。研究之重點則依產業界之需求，在鼓勵教師成立研究群，協同產業界進行跨領域研發工作，現階段研究重點在於計算科學、數學資訊教育、遊戲設計、品質管制與生物統計等領域。除提昇學術能量外，也積極推動產、官、學之合作機制。",
        },
        {
          title: "優質教學的成果豐碩",
          img: "http://www.math.fcu.edu.tw/2021_new_website/data/img/Characteristic3.jpg",
          context:
            "本系在優質教學的成果豐碩，「數學網路教學實驗室」等網站皆榮獲教育部A級網站評等，近年來致力於大學數學教育，與「中部區域教學中心」合作，成立中區微積分中心，利用專業知識與電腦技術，提供數位教材與創新教材教法，提昇學生學習成就，廣受各界肯定，相關技術也應用於線性代數、數值分析等教學，讓學習數學不再是困難重重。在良好的數學基礎下，導入學程、遊戲設計、網格生成、品質管制、財務金融等實用課程，讓學生就業無障礙，成果顯著。",
        },
      ],
    };
  },
};
</script>
<style scoped>
.el-row {
  display: flex;
  flex-wrap: wrap;
  padding: 12px 0px;
}

.el-card {
  height: 100%;
}
.el-card h5 {
  font-weight: 600;
}

img {
  display: block;
  width: 100%;
  max-width: 100%;
  margin: 0;
  height: 100%;
  object-fit: cover;
}
</style>

