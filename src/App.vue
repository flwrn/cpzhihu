<template lang="html">
  <div>
    <explore-header></explore-header>
    <div class="main">
      <div class="center clearfix">
        <div v-bind:class="mainColClass">
          <editor-recommendation></editor-recommendation>
          <top-question-list></top-question-list>

        </div>
        <div v-bind:class="sideColClass">
          <sign-up-zhihu></sign-up-zhihu>
          <download-zhihu-btn></download-zhihu-btn>
          <hot-tables></hot-tables>
          <hot-topics></hot-topics>
          <hot-favs></hot-favs>
          <app-footer></app-footer>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import ExploreHeader from './components/ExploreHeader.vue';
import SignUpZhihu from './components/SignUpZhihu.vue';
import EditorRecommendation from './components/EditorRecommendation.vue';
import TopQuestionList from './components/TopQuestionList.vue';
import DownloadZhihuBtn from './components/DownloadZhihuBtn.vue';
import HotTables from './components/HotTables.vue';
import HotTopics from './components/HotTopics.vue';
import HotFavs from './components/HotFavs.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    'explore-header': ExploreHeader,
    'sign-up-zhihu': SignUpZhihu,
    'editor-recommendation': EditorRecommendation,
    'top-question-list': TopQuestionList,
    'download-zhihu-btn': DownloadZhihuBtn,
    'hot-tables': HotTables,
    'hot-topics': HotTopics,
    'hot-favs': HotFavs,
    'app-footer': Footer
  },
  data() {
    return {
      mainColClass: {
        'col-l': true,
        'f-l': true
      },
      sideColClass: {
        'col-s': true,
        'f-r': true
      }
    }
  },
  methods: {
    resizeWidth: function() {
      if (screen.availWidth <= 1000) {
        this.mainColClass['col-l'] = false;
        this.mainColClass['f-l'] = false;
        this.sideColClass['col-s'] = false;
        this.sideColClass['f-r'] = false;
      } else {
        this.mainColClass['col-l'] = true;
        this.mainColClass['f-l'] = true;
        this.sideColClass['col-s'] = true;
        this.sideColClass['f-r'] = true;
      }
    },
    showMoreQuestions() {
      console.log(this);
    }
  },
  mounted() {
    this.$nextTick(() => {
      window.onresize = () => {
        this.resizeWidth();
        console.log(screen.availWidth);
      }
      this.resizeWidth();
    });
  }
}



</script>

<style lang="scss">
  .main {
    margin: 80px 0;
  }
</style>
