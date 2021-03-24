<template>
  <v-app id="inspire">
    <v-app-bar app color="rgb(250, 250, 250)">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <!-- Application -->
        <v-icon x-large>mdi-cart</v-icon>
      </v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" fixed temporary>
      <!--  -->
    </v-navigation-drawer>

    <v-main class="lighten-2">
      <v-container>
        <v-row>
          <Carousel/>
        </v-row>
        <v-row>
          <template v-for="n in 4">
            <v-col :key="n" class="mt-2" cols="12">
              <strong>Category {{ n }}</strong>
            </v-col>

            <v-col v-for="j in 3" :key="`${n}${j}`" cols="3" md="4">
              <!-- <v-sheet height="150"></v-sheet> -->
              <v-card class="mx-auto" elevation="10" tile>
                <v-img
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img>
                <v-card-title class="font-weight-medium">
                  我是中文
                </v-card-title>
                <v-card-subtitle>
                  Health Eat均衡餐盤 *五大特色* 1.均衡攝取各類營養素
                  2.可靈活運用於飲食模式(高蛋白.低醣)控制慢性病
                  3.食物分格，乾淨舒適，細細品嚐不同滋味
                  4.木製時尚具有保溫與溫暖風韻
                  5.100%圓角設計、容易取食、好清潔、不卡垢 【注意事項】
                  1.嚴禁洗(烘)碗機、烤箱、微波爐。 2.勿使用強酸或強鹼清潔劑。
                  3.商品有破損或破裂，請立即汰換，確保安全。 【清潔方式】
                  1.使用洗碗精以海綿洗淨。 2.充分擦乾，室內保存即可。
                  【商品規格】 尺寸:27cm × 21cm × 2cm(深)
                  材質:橡膠木拼板、山毛櫸拼板 表面塗料:環安水性漆(SGS檢驗合格)
                  【不發霉 🚫 宣言】 存放半年的儲藏性試驗(室溫通風良好環境)
                  100次的食用測試 ✖ 100次的清洗測試 就是不會發霉🕵
                </v-card-subtitle>

                <v-card-text>
                  <div>定價</div>
                  <div>NT 1000</div>
                </v-card-text>
                <v-card-actions>
                  <v-btn color="deep-purple lighten-2" text @click="reserve">
                    Reserve
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Carousel from '@/components/Carousel'
export default {
  name: 'index',
  components: { Carousel },
  data: () => ({ drawer: null })
}
</script>
