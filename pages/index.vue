<template>
  <div class="container">
    <div class="catalog-container">
      <div class="catalog-wrapper">
        <div>
          <button @click="showAddDialog">添加</button>
        </div>
        <dl>
          <dt>分类</dt>
          <dd>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
          </dd>
          <dt>分类</dt>
          <dd>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
            <a href="#">导航</a>
          </dd>
        </dl>
      </div>
    </div>
    <dialog ref="addDialog">
      <form action="">
        <label for="name">
          名称
          <input id="name" type="text" />
        </label>
        <label for="address">
          网址
          <input id="address" type="text" />
        </label>
        <label for="catalog">
          分类
          <select id="catalog" type="text">
            <option value="0">未分类</option>
          </select>
        </label>
      </form>
      <button @click="closeDialog">关闭</button>
      <button @click="closeDialog">关闭</button>
    </dialog>
  </div>
</template>

<script>
export default {
  components: {},
  methods: {
    showAddDialog() {
      this.$refs.addDialog.show()
    },
    closeDialog() {
      this.$refs.addDialog.close()
    }
  }
}
</script>

<style>
.catalog-container {
  width: 895px;
  margin: 10px auto;
  border: 1px solid #e9e9e9;
}
.catalog-wrapper {
  width: 844px;
  margin: 0 auto;
  padding: 10px 0;
}
</style>
