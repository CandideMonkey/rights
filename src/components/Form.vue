<template>
    <div>
        <el-form ref="form" :model="form" label-width="80px">
            <el-form-item label="欠薪企业">
                <el-input v-model="form.name"></el-input>
            </el-form-item>
            <el-form-item label="企业类型">
                <el-select v-model="form.region" placeholder="请选择企业类型">
                    <el-option label="互联网企业" value="internet"></el-option>
                    <el-option label="电商平台企业" value="e-com"></el-option>
                    <el-option label="区块链企业" value="blockchain"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="欠薪时间">
                <el-date-picker
                        v-model="value6"
                        type="daterange"
                        range-separator="至"
                        start-placeholder="开始日期"
                        end-placeholder="结束日期">
                </el-date-picker>
            </el-form-item>
            <el-form-item label="是否追回">
                <el-switch v-model="form.delivery"></el-switch>
            </el-form-item>
            <el-form-item label="欠薪原因">
                <el-checkbox-group v-model="form.type">
                    <el-checkbox label="公司倒闭" name="type"></el-checkbox>
                    <el-checkbox label="道德绑架" name="type"></el-checkbox>
                    <el-checkbox label="有钱不还" name="type"></el-checkbox>
                    <el-checkbox label="就是欠" name="type"></el-checkbox>
                </el-checkbox-group>
            </el-form-item>

            <el-form-item label="补充">
                <el-input type="textarea" v-model="form.desc"></el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="onSubmit">提交</el-button>
                <el-button>取消</el-button>
            </el-form-item>
        </el-form>

    </div>
</template>

<script>
  export default {
    name:"Form",
    data() {
      return {
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        }
      }
    },
    methods: {
      onSubmit() {

      }
    }
  }
</script>

<style scoped>

</style>