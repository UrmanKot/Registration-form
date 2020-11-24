<template>
    <div class="check-in">
        <p class="check-in__text">Вы успешно зарегистрировались!</p>
        <button class="check-in__button button" @click="resetForm">Назад</button>
    </div>
</template>

<script>
export default {
    methods: {
        resetForm() {
            this.$emit('reset-form');
        }
    }
}
</script>

<style lang="scss">
    .check-in {
        max-width: 400px;
        width: 100%;
        padding: 30px;
        border: 4px solid #f0f0f0;
        text-align: center;
        position: fixed;
        top: 30%;
        left: 50%;
        margin-left: -200px;
    }

    .check-in__text {
        margin-bottom: 30px;
        line-height: 1.4;
    }

    .check-in__button {
        margin: 0 auto;
        width: 100%;
    }

    @media (max-width: 768px) {
        .check-in {
          margin: 70px auto 0;
          position: inherit;
          width: auto;
        }
    }
</style>