<template>
    <div class="home-page">
        <div class="bg" />
        <div class="login">
            <div class="logo">
                <img src="/logo.png">
            </div>
            <user-area />
        </div>
    </div>
</template>

<script>
export default {
    layout: 'home',
    created () {
        if (this.token) {
            this.$router.push('/home')
        }
    }
}
</script>

<style lang="scss" scoped>
.bg {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    background: url('/bg.png');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    z-index: -1;
}
.login {
    width: 20vw;
    margin: 150px;

    .logo {
        img {
            margin-bottom: 30px;
            width: 100%;
        }
    }

    .grid {
        margin-top: 30px;
        width: 100%;
        display: grid;
        grid-template-columns: 2fr 1fr;
        grid-gap: 20px;
    }
}
</style>
