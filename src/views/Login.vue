<script setup>
import headerLogin from '../components/login/headerLogin.vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="login-container">
        <div class="login-header">
            <headerLogin></headerLogin>
        </div>
        <div class="form-login">
            <div class="form-login-card">
                <p class="form-login-title">Entre na sua conta</p>
                <p>Para acessar sua conta informe seu e-mail e senha</p>
                <div class="form-login-inputs">
                    <label for="email">E-mail</label>
                    <br>
                    <input class="form-login-inputs-field" type="email" id="email" placeholder=" Seu e-mail" v-model="email">
                    <br>
                    <label for="password">Senha</label>
                    <br>
                    <input class="form-login-inputs-field" type="password" id="password" placeholder=" Sua senha" v-model="password">
                </div>
                <div class="form-login-forgot-password">
                    <p>Esqueci minha senha</p>
                </div>
                <div class="form-login-btn">
                    <button class="form-login-btn-submit" type="submit">FAZER LOGIN</button>
                </div>
            </div>
        </div>
        <div class="form-login-signup">
            <p>Ainda nao tem conta? <RouterLink to="/product-plans">Cadastra-se</RouterLink></p>
            <router-view></router-view>
        </div>
        <div class="login-footer"></div>
    </div>
</template>

<style scoped>
.login-container {
    height: 100vh;
    width: 100vw;
}

.login-header {
    display: flex;
    justify-content: center;
    margin-top: 200px;
}

.form-login {
    display: flex;
    justify-content: center;
}
.form-login-card {
    margin: 30px 0;
    width: 100%;
    max-width: 700px;
    background-color: white;
    border: 2px solid #e6eaf2;
    border-radius: 3px;
    padding: 30px;
}

.form-login-title {
    font-weight: bolder;
    font-size: 30px;
}

.form-login-inputs-field {
    width: 100%;
    height: 50px;
    border-radius:5px;
    border:1px solid #a8aeba;
}

.form-login-forgot-password {
    display: flex;
    justify-content: end;
}

.form-login-btn {
    width: 100%;
}

.form-login-btn-submit {
    margin-top: 20px;
    width: 100%;
    height: 50px;
    color: white;
    border: none;
    border-radius:5px;
    background-color: #f30168;
}
.form-login-signup {
    display: flex;
    justify-content: center;
}
</style>