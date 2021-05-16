<template>
  <div class="container-fluid mt-4">
    <div class="row">
      <div class="col-6">
        <Pagination />
        <FilterTable />
        <TableUsers />
      </div><!-- col-6 -->
      <div class="col-6">
        <PaginationReusable />
        <FilterTableReusable />
        <TableUsersReusable />
      </div><!-- col-6 -->
    </div><!-- row -->
  </div>
</template>

<script>
import FilterTable from './FilterTable.vue'
import TableUsers from './TableUsers';
import Pagination from './Pagination';

import FilterTableReusable from './reusable/FilterTable.vue'
import TableUsersReusable from './reusable/TableUsers';
import PaginationReusable from './reusable/Pagination';

export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  components: {
    TableUsers,
    FilterTable,
    Pagination,
    FilterTableReusable,
    TableUsersReusable,
    PaginationReusable
  },
  computed:{
  },
  methods:{
  },
  beforeCreate() {
    this.$store.dispatch("getPosts");
  },
  mounted(){
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
