<template>
    <div id="app">
        <div>
            <el-button @click="startHacking">Start</el-button>
            <el-input placeholder="Please input" v-model="input1"></el-input>
            <el-time-select
                    v-model="input2"
                    :picker-options="{
    start: '08:30',
    step: '00:15',
    end: '18:30'
  }"
                    placeholder="Select time">
            </el-time-select>
            <el-switch v-model="value1">
            </el-switch>
        </div>
    </div>
</template>

<script>
  export default {
    data:function(){
      return{
        value1:""
      }
    },
    methods: {
      startHacking() {
        this.$notify({
          title: 'It works!',
          type: 'success',
          message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
          duration: 5000,
        });
      },
    },
  };
</script>

<style>
    #app {
        font-family: Helvetica, sans-serif;
        text-align: center;
    }
</style>
