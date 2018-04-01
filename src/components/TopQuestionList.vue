<template lang="html">
  <div class="top-question">
    <div class="tabs clearfix">
      <ul>
        <li><a href="#" class="top-today f-l">今日最热</a></li>
        <li><a href="#" class="top-month f-l">本月最热</a></li>
      </ul>
    </div>
    <div class="question-list">
      <ul>
        <li class="clearfix" v-for="question in questionList" v-on:mouseenter="question.hover=true" v-on:mouseleave="question.hover=false">
          <a href="#" class="question"><h4>{{question.question}}</h4></a>
          <a href="#" class="likes f-l">{{question.likes}}</a>
          <div class="author">
            <a href="#" class="name"><h4>{{question.author.name}}</h4></a>
            <a href="#" class="field">{{question.author.field}}</a>
            <p class="info">{{question.author.info}}</p>
          </div>
          <p class="answer">{{question.answer}}</p>
          <div class="btns clearfix">
            <ul class="clearfix f-l">
              <li class="f-l"><a href="#" class="follow-btn">关注问题</a></li>
              <li class="f-l"><a href="#" class="comments">{{question.comments}}条评论</a></li>
            </ul>
            <ul class="clearfix f-l" v-if="!question.hover">
              <li class="f-l"><a href="#" class="ask-repost">申请转载</a></li>
            </ul>
            <ul class="clearfix f-l" v-if="question.hover">
              <li class="f-l"><a href="#" class="thank">感谢</a></li>
              <li class="f-l"><a href="#" class="share">分享</a></li>
              <li class="f-l"><a href="#" class="favorite">收藏</a></li>
              <li class="f-l"><a href="#" class="helpless">没有帮助</a></li>
              <li class="f-l"><a href="#" class="">举报</a></li>
              <li class="f-l"><a href="#" class="no-repost">禁止转载</a></li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      questionList: [
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        },
        {
          question: '一个问题',
          likes: 666,
          author: {
            name: '作者名字',
            field: '，某某问题的优秀回答者',
            info: '信息介绍'
          },
          answer: '回答的具体内容...',
          comments: 233,
          hover: false
        }
      ]
    }
  },
  methods: {
    showList() {
      console.log(this.list);
    }
  },
  computed: {
    list() {
      return document.querySelectorAll('.top-question .question-list > ul > li');
    }
  }
}
</script>

<style lang="scss" scoped>
  .top-question {
    margin: 10px 0;
    .tabs {
      margin: 10px 0;
      a {
        margin-right: 5px;
        padding: 5px 10px;
        border-radius: 2px 2px 0 0;
        border-left: 1px solid #ddd;
        border-right: 1px solid #ddd;
        border-top: 1px solid #ddd;
        color: #666;
      }
    }
    .question-list {
      &>ul>li {
        margin: 10px 0;
        border-bottom: 1px solid #ccc;
        &:last-of-type {
          border-bottom: 0;
        }
      }
      .question {
        color: #06c;
        margin: 5px 0;
      }
      .likes {
        background: #eff;
        color: #009;
        border-radius: 2px;
        padding: 5px;
      }
      .author, .answer, .btns {
        margin: 5px 0 5px 50px;
      }
      .author {
        * {
          display: inline;
          color: #000;
        }
      }
      .btns {
        a {
          padding: 0 5px;
          color: #666;
        }
      }
    }
  }
</style>
