<template>
    <div>
       
        <main>
            <div class="container">
                <h1>Бургеры</h1>
                <div class="main-cards">
                    <section class="main-cards-item" v-for="item in 12" :key="item">
                        <img class="main-cards-item__img" src="../assets/images/pizza.jpg" alt="jpg">
                        <h3 class="main-cards-item__title">Spain Jalapeno Burger</h3>
                        <p class="main-cards-item__text">43 000 сум</p>
                        <button class="main-cards-item__btn">
                            корзина
                        </button>
                    </section>
                </div>
            </div>
        </main>

    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>