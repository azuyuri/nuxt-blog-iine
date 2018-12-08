<template>
  <section>
    <el-card>
      <div>
        <el-input />
      </div>
      <div>
        <el-input />
      </div>
      <div class="">
        <el-button>
          <span />
          <span>Publish</span>
        </el-button>
      </div>
    </el-card>
  </section>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
  asyncData({ redirect, store }) {
    if (!store.getters['user']) {
redirect('/')
    }

    return {
      formData: {
        title: '',
        body: ''
      }
    }
  },
  computed: {
    ...mapGetters(['user'])
  },

  methods: {
    publish() {
    }
  }
}
</script>

<style>
.post-page .el-table__row {
  cursor: pointer;
}
</style>


