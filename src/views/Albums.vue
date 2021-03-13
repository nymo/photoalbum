<template>
  <div class="home">
    <h1>Albums</h1>
    <List></List>
  </div>
</template>

<script>

import ListTable from "@/components/ListTable";

export default {
  name: 'Albums',
  components: {
    'List': ListTable,
  }
}
</script>
