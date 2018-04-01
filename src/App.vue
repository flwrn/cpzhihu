<template lang="html">
  <div>
    <explore-header></explore-header>
    <div class="main">
      <div class="center clearfix">
        <div class="col-l f-l">
          <editor-recommendation></editor-recommendation>
          <top-question-list></top-question-list>
          <a class="more">更多</a>
        </div>
        <div class="col-s f-r">
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
  }
}
</script>

<style lang="scss">
  .main {
    margin: 80px 0;
    .more {
      background: #eee;
      text-align: center;
      height: 40px;
      color: #999;
      line-height: 40px;
      border-radius: 2px;
      border: 1px solid #ccc;
      box-shadow: 0 1px 5px #ccc;
      margin: 10px;
    }
  }
</style>
