<template>
    <div class="main-login">
        <div>
            <img src="../assets/svgs/image1.svg" alt="">
        </div>
        <div class="login-form">
            <h1 class="title-form">LOGIN</h1>
            <form class="form" v-on:submit.prevent="login">
                <div class="input-wrapper">
                    <input type="email" name="email" id="email" v-model="email" />
                    <span class="icon">
                        <img src="../assets/svgs/user (2) 1.svg" alt="">
                    </span>
                </div>
                <div class="input-wrapper">
                    <input type="password" name="password" id="password" v-model="password" />
                    <span class="icon">
                        <img src="../assets/svgs/lock 1.svg" alt="">
                    </span>
                </div>
                <p class="forgot">lupa password?</p>
                <button class="login-btn" type="submit">MASUK</button>
                <p class="register-text">belum punya akun? <a href="#">daftar sekarang</a></p>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            email: "",
            password: ""
        }
    }, methods: {
        login() {

        }
    }
}
</script>

<style scoped>
.main-login {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 990px;
    height: 550px;
    gap: 130px;
    margin-top: 20px;
}

.login-form {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    align-content: center;
    width: 100%;
    height: 100%;
    gap: 15px;
}

.title-form {
    font-size: 43px;
    color: var(--color-title);
    padding: 0;
    text-align: center;
    margin-bottom: 40px;
    width: 110px;
    height: 42px;
}

.form {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 15px;
}

.input-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
}

.input-wrapper {
    width: 355px;
    height: 55px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 30px;
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 0 20px;
    margin-bottom: 18px;
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.08);
    backdrop-filter: blur(10px);
}

.input-wrapper svg {
    width: 22px;
    opacity: 0.7;
}

.input-wrapper input {
    width: 351px;
    height: 52px;
    padding-left: 9px;
    border: none;
    background-color: #f3f6ff;
    border-radius: var(--radius);
    outline: none;
    transition: var(--transition);
    color: var(--color-text);
    font-family: var(--font-primary);
    font-size: 16px;
    font-weight: 400;
    line-height: 24px;
    letter-spacing: 0.15px;
    text-align: left;
    position: absolute;
    margin-left: 13px;
}

.login-form button {
    width: 335px;
    height: 52px;
    border-radius: 5px;
    border: none;
    background-color: var(--color-btn);
    color: var(--color-bg);
    cursor: pointer;
}

.forgot {
    text-align: right;
    margin: -10px 10px 25px 0;
    font-size: 14px;
    color: #777;
}

.login-btn {
    width: 362px;
    height: 52px;
    border-radius: 9999px;
    border: none;
    background-color: var(--color-btn);
    color: var(--color-bg);
    cursor: pointer;
}

.register-text {
    font-size: 14px;
    color: var(--color-title);
}

.register-text a {
    color: #000;
    font-weight: bold;
    text-decoration: none;
}

.icon {
    margin-left: -10px;
}
</style>