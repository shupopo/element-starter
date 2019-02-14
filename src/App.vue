<template>
    <div id="app">
        <el-container>
            <el-header height="100px">
            </el-header>
            <el-container>
                <el-aside width="200px">
                    <el-col :span="24">
                        <el-menu default-active="1" class="el-menu-vertical-demo">
                            <el-menu-item index="1">
                                <i class="el-icon-location"></i>
                                <router-link to="/location"><span>Location</span></router-link>
                            </el-menu-item>
                            <el-menu-item index="2" disabled>
                                <i class="el-icon-document"></i>
                                <!-- 6. When clicking, it loads the contents defined in 2 and 1 -->
                                <router-link to="/foo"><span>foo</span></router-link>
                            </el-menu-item>
                            <el-menu-item index="3">
                                <i class="el-icon-setting"></i>
                                <span>Navigator Four</span>
                                <router-link to="/bar"><span>bar</span></router-link>
                            </el-menu-item>
                        </el-menu>
                    </el-col>
                </el-aside>
                <el-main>
                    <el-table :data="location" style="width: 100%">
                        <el-table-column prop="id" label="id" width="100"></el-table-column>
                        <el-table-column prop="name" label="name"></el-table-column>
                        <el-table-column prop="country" label="country" width="180"></el-table-column>
                        <el-table-column prop="metro" label="metro" width="180"></el-table-column>
                        <el-table-column prop="market" label="market" width="180"></el-table-column>
                        <el-table-column prop="status" label="status" width="180"></el-table-column>
                    </el-table>
                </el-main>
            </el-container>
        </el-container>


    </div>
</template>

<script>
  export default {
    data: function() {
      return {
        value1: '',
        location: [
          {id: 1, name: 'Site1', country: 'USA', metro: 'San Jose', market: 'US', status: 'Active'},
          {id: 2, name: 'Site2', country: 'USA', metro: 'San Mateo', market: 'US', status: 'Active'},
          {id: 3, name: 'Site3', country: 'USA', metro: 'San Rafael', market: 'US', status: 'Active'}],

      };
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
