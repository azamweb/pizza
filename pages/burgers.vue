<template>
    <div>
        <main>
            <div class="container">
                <h1>Hot-Dog</h1>
                <div class="burgers-cards">
                    <section class="burgers-cards-item" v-for="item in 5" :key="item">
                        <img class="burgers-cards-item__img" src="../assets/images/pizza.jpg" alt="jpg">
                        <h3 class="burgers-cards-item__title">Spain Jalapeno Burger</h3>
                        <p class="burgers-cards-item__text">43 000 сум</p>
                        <button class="burgers-cards-item__btn">
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