<template>
  <div>
    <Header />
    <div class="content">
      <!-- <div class="form-group row"> -->
      <label for="search" class="col-4 col-form-label">Name</label>
      <div class="col-8">
        <input
          type="text"
          class="form-control"
          id="search"
          placeholder="Please input"
          v-model="searchInput"
        />
      </div>
      <!-- </div> -->
    </div>
    <div class="content-button">
      <button type="button" class="btn btn-secondary">Search</button>
      <button type="button" class="btn btn-warning" @click="clearInput()">
        Clear
      </button>
      <button type="button" class="btn btn-primary">Add</button>
    </div>
    <br />
    <hr />
    <div class="content-result">
      <div class="d-flex justify-content-start mb-3">Search result</div>
      <div v-for="(data, i) in nameTest" :key="i">
          <Result :name="data.name" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '../components/Header.vue'
import Result from '../components/Result.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Result
  },
  data () {
    return {
      searchInput: '',
      nameTest: [
        {
          name: 'Test 1'
        },
        {
          name: 'Test 2'
        },
        {
          name: 'Test 3'
        },
        {
          name: 'Test 4'
        },
        {
          name: 'Test 5'
        }
      ]
    }
  },
  methods: {
    clearInput () {
      this.searchInput = ''
    }
  }
}
</script>

<style>
.content-result {
  width: 75%;
  margin-left: 50px;
  float: left;
}

.content {
  margin-left: 50px;
  margin-top: 20px;
  display: grid;
  grid-template-columns: 10% 20%;
  gap: 15px;
}

.content-button {
  margin-top: 30px;
  display: grid;
  grid-template-columns: 13% 13% 13%;
  gap: 25px;
  justify-content: center;
}
</style>
