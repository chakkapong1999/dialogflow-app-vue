<template>
  <div class="result-list">
    <li class="list-item">
      <div class="row">
        <div class="col-6 left">{{ name }}</div>
        <div class="col-6 right">
          <button class="btn bg-transparent"><b-icon-pencil-square /></button>
        </div>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: 'Result',
  props: {
    name: {
      type: String
    }
  }
}
</script>

<style>
.left {
  text-align: left;
}

.right {
  text-align: right;
}

.result-list {
  margin-left: 50px;
  justify-content: center;
}
.list-item {
  padding: 10px;
  border: 1px solid rgba(128, 128, 128, 0.5);
  border-radius: 3px;
  list-style-type: none;
}
</style>
