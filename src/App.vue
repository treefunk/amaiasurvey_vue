<template>
  <div id="app">
    
    <div id="mainapp" v-if="valid">
      <Header />
      <Breadcrumbs />
      <section class="questionnaire">
        <div class="pagewrapper2">
            <QuestionCount />
        <BuyingExperience />
        <SiteVisitExperience />
        <ShowroomSales />
        <Product />
        <HomeBuyingDecision />
        <Agreement />
        <PrevNext/>
        </div>
      </section>
    </div>
    <div v-else>
      404
    </div>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Breadcrumbs from './components/Breadcrumbs.vue'
import PrevNext from './components/PrevNext.vue'
import QuestionCount from './components/QuestionCount.vue'

//Questions
import BuyingExperience from './components/BuyingExperience.vue'
import SiteVisitExperience from './components/SiteVisitExperience.vue'
import ShowroomSales from './components/ShowroomSales.vue'
import Product from './components/Product.vue'
import HomeBuyingDecision from './components/HomeBuyingDecision.vue'
import Agreement from './components/Agreement.vue'
//

import { mixin } from './mixins/mixin.js'


//Routes

export default {
  data(){
    return {
      valid: true // set to true for testing :)
    }
  },
  name: 'app',
  mixins: [ mixin ],
  components: {
    QuestionCount,
    Header,
    Breadcrumbs,
    PrevNext,
    BuyingExperience,
    SiteVisitExperience,
    ShowroomSales,
    Product,
    HomeBuyingDecision,
    Agreement
  }
}
</script>

<style>

</style>
