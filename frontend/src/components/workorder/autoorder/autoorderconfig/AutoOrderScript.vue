<template>
    <div class="autoorderscript">
        <el-row>
            <el-input v-model="script" placeholder="请输入脚本位置"></el-input>
        </el-row>
        <el-row style="text-align:left;">
            <el-button @click="handleSaveScript" size="mini">保存</el-button>
        </el-row>
    </div>
</template>

<script>
export default {
    name: 'autoorderscript',
    data () {
        return {
            script: '',
        }
    },
    props: {
        ordertypescript: {
            type: String
        },
        saveAutoOrderScript: {
            type: Function
        },
    },
    watch:  {
        ordertypescript(val) {
            this.script = this.ordertypescript
        }
    },
    methods: {
        handleSaveScript () {
            if (this.script) {
                this.saveAutoOrderScript(this.script)
            }
            
        },
    }
}
</script>

<style>

</style>