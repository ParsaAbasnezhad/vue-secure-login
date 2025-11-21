<template>
    <header class="header">
        <div class="title">Shoply.</div>
        <div class="menu">
            <router-link class="header-link" to="/">Home</router-link>
            <span class="dash">/</span>
            <router-link class="header-link" to="/login">Products</router-link>
            <span class="dash">/</span>
            <router-link class="header-link" to="/register">About</router-link>
        </div>
        <div class="actions">
            <div>
                <svg width="29" height="32" viewBox="0 0 29 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g clip-path="url(#clip0_106_166)">
                        <path
                            d="M10.7695 29.3332C11.4303 29.3332 11.966 28.7362 11.966 27.9998C11.966 27.2635 11.4303 26.6665 10.7695 26.6665C10.1086 26.6665 9.57288 27.2635 9.57288 27.9998C9.57288 28.7362 10.1086 29.3332 10.7695 29.3332Z"
                            stroke="#616467" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        <path
                            d="M23.9316 29.3332C24.5924 29.3332 25.1281 28.7362 25.1281 27.9998C25.1281 27.2635 24.5924 26.6665 23.9316 26.6665C23.2707 26.6665 22.735 27.2635 22.735 27.9998C22.735 28.7362 23.2707 29.3332 23.9316 29.3332Z"
                            stroke="#616467" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        <path
                            d="M1.19653 1.3335H5.98286L9.18969 19.1868C9.29911 19.8007 9.59881 20.3521 10.0363 20.7446C10.4738 21.137 11.0213 21.3455 11.5829 21.3335H23.2136C23.7752 21.3455 24.3226 21.137 24.7601 20.7446C25.1977 20.3521 25.4974 19.8007 25.6068 19.1868L27.5213 8.00016H7.17944"
                            stroke="#616467" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </g>
                    <rect x="0.5" y="0.5" width="27.7179" height="31" stroke="black" />
                    <defs>
                        <clipPath id="clip0_106_166">
                            <rect width="28.7179" height="32" fill="white" />
                        </clipPath>
                    </defs>
                </svg>
            </div>
            <router-link class="login-link" @click.prevent.enter="loginCenter">
                {{ isLogin ? 'Login' : 'Register' }}
            </router-link>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            isLogin: true
        }
    },
    methods: {
        loginCenter() {
            this.$emit(this.isLogin ? 'login' : 'register')
            this.isLogin = !this.isLogin
        }
    }
}
</script>

<style scoped>
.header {
    display: flex;
    width: 96rem;
    height: 115px;
    justify-content: center;
    align-content: center;
    align-items: center;
    gap: 330px;
    background-color: var(--color-hedear);
}

.title {
    font-size: 39px;
    color: var(--color-title);
    padding: 0;
    text-align: center;
    margin-bottom: 40px;
    width: 99px;
    height: 35px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: auto;
}

.menu {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 5rem;
}

.header-link {
    width: 44px;
    height: 19px;
    color: var(--color-text);
    text-decoration: none;
    cursor: pointer;
}

.dash {
    color: var(--color-dash);
}

.actions {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px;
}

.login-link {
    width: 113px;
    text-align: center;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--color-btn);
    color: var(--color-bg);
    border: none;
    border-radius: 2px;
    cursor: pointer;
}

.login-link:hover {
    background-color: #2e2b27;
    transform: translateY(-2px);
    box-shadow: 0 6px 18px rgba(0, 0, 0, 0.25);
}

.login-link:active {
    transform: translateY(0px) scale(0.98);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
}
</style>
