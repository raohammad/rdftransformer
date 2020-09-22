<template>
  <div class="transformer">
    <br/>
    <SingleFile/>
    <br/>
    <DataTransformer msg="fukhtakhin"/>
  </div>
</template>

<script>
// @ is an alias to /src
import DataTransformer from '@/components/DataTransformer.vue'
import SingleFile from '@/components/SingleFile.vue'

export default {
  name: 'transformer',
  components: {
    DataTransformer,
    SingleFile
  }
}
</script>
