<template>
    <div>
        <el-form id="form" :label-position="labelPosition" label-width="100px" :model="loginForm">
            <el-form-item label="ID">
                <el-input v-model="loginForm.id"></el-input>
            </el-form-item>
            <el-form-item label="PWD">
                <el-input type="password" v-model="loginForm.pwd"></el-input>
            </el-form-item>
            <el-form-item>
                <el-button @click="onSubmit">LOG IN</el-button>
            </el-form-item>
        </el-form>
    </div>
</template>
<script>
    export default {
        name : 'LogIn', 
        data() {
            return {
                labelPosition: 'left',
                loginForm: {
                    id: '',
                    pwd: ''
                }
            };
        },
        methods : {
            onSubmit() {
                console.log(this.loginForm);
            }
        }
    }

</script>
<style>
    #form {
        width: 300px;
        margin: auto;
        top:300px;
    }
</style>