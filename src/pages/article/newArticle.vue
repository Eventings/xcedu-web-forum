<template>
  <section class="app-forum-create">
    <section class="app-forum-navbar">
      <div>
        <Logo />
        <div class="app-forum-navbar-title">
          <h3 class="size-large-x">内容发布</h3>
        </div>
        <el-button type="primary" @click="submit">发布</el-button>
        <el-button type="default" @click="goBacktToHome">返回首页</el-button>
      </div>
    </section>
    <div class="app-forum-container">
      <newArticle :flag="flag" />
    </div>
  </section>
</template>
<script>
import newArticle from '@page/components/compose'
export default {
  components: {
    newArticle
  },
  data () {
    return {
      flag: 0
    }
  },
  methods: {
    submit (data) {
      this.flag++
    },
    goBacktToHome () {
      this.$router.push({ name: 'home' })
    }
  }
}
</script>
