<template>
    <div>

      
       
        <header class="header">
            <div class="container">
                <NuxtLink to="/">
                    <img class="header-img" src="../assets/images/pizza.jpg" alt="jpg">
                </NuxtLink>
                <div class="header-search">
                    <span>
                        <img class="header-search-img" src="../assets/images/search.svg" alt="search">
                    </span>
                    <input type="text" placeholder="searching">
                </div>

                <div class="header-top-items">
                    <NuxtLink to="/burgers" class="header-top-items-section">
                        <img class="header-top-items-section__img" src="../assets/images/pizza.svg" alt="pizza">
                        <p class="header-top-items-section__text">burger</p>
                    </NuxtLink>
                    <NuxtLink to="/" class="header-top-items-section">
                        <img class="header-top-items-section__img" src="../assets/images/pizza.svg" alt="pizza">
                        <p class="header-top-items-section__text">burger</p>
                    </NuxtLink>
                    <NuxtLink to="/" class="header-top-items-section">
                        <img class="header-top-items-section__img" src="../assets/images/pizza.svg" alt="pizza">
                        <p class="header-top-items-section__text">burger</p>
                    </NuxtLink>
                    <NuxtLink to="/" class="header-top-items-section">
                        <img class="header-top-items-section__img" src="../assets/images/pizza.svg" alt="pizza">
                        <p class="header-top-items-section__text">burger</p>
                    </NuxtLink>
                    <NuxtLink to="/" class="header-top-items-section">
                        <img class="header-top-items-section__img" src="../assets/images/pizza.svg" alt="pizza">
                        <p class="header-top-items-section__text">burger</p>
                    </NuxtLink>
                </div>

            </div>
        </header>

        <div class="basket-wrapper" v-if="basket">
            <div class="basket">
                <div class="container">
                    <div class="basket-top">
                        <h1 class="basket-title">
                            Корзина
                        </h1>
                        <img @click="basket = false" src="../assets/images/remove.svg" alt="remove" class="basket-top__img">
                    </div>
                    <section class="basket-item">
                        <img class="basket-item__img" src="../assets/images/burger.svg" alt="burger">
                        <h2 class="basket-item__title">Корзина пуста</h2>
                        <p class="basket-item__text">Воспользуйтесь поиском или каталогом, чтобы найти товары</p>
                    </section>
                </div>
            </div>
        </div>

        <div class="menu-wraper" v-if="menu">
            <div class="menu">
                <div class="container">
                    <div class="manu-top">
                        <h1 class="manu-top__title">Меню</h1>
                        <img @click="menu = false" src="../assets/images/remove.svg" alt="remove" class="manu-top__img">
                    </div>

                    <nav class="manu-nav">
                        <ul class="menu-nav-list">
                            <li class="menu-nav-list-item" v-for="item in 7" :key="item">
                                <NuxtLink class="menu-nav-list-item__link" to="/">Бургеры</NuxtLink>
                                <img class="menu-nav-list-item__img" src="../assets/images/chevronright.svg" alt="sss">
                            </li>
                        </ul>
                    </nav>
                    
                </div>
            </div>
        </div>

        <div class="register-wraper" v-if="register">
            <div class="register">
                <div class="container">
                    <div class="register-top">
                        <h1 class="register-top__title">Авторизация</h1>
                        <img @click="register = false" src="../assets/images/remove.svg" alt="remove" class="register-top__img">
                    </div>

                    <section class="register-item">
                        <img src="../assets/images/burger.svg" alt="burger" class="register-item__img">
                        <form>
                            <input class="register-item-input" type="number" placeholder="number phone">

                            <button class="register-item-btn">
                                send code
                            </button>
                        </form>
                    </section>

                </div>
            </div>
        </div>

        <div class="search-wraper" v-if="search">
            <div class="search">
                <div class="container">
                    <div class="search-top">
                        <h1 class="search-top__title">Поиск</h1>
                        <img @click="search = false" src="../assets/images/remove.svg" alt="remove" class="search-top__img">
                    </div>

                    <div class="search-input">
                        <span>
                            <img class="search-input-img" src="../assets/images/search.svg" alt="search">
                        </span>
                        <input type="text" placeholder="searching">
                    </div>

                    <section class="search-item">
                        <img src="../assets/images/burger.svg" alt="burger" class="search-item__img">
                        <h1 class="search-item__title">Начните поиск</h1>
                    </section>

                </div>
            </div>
        </div>

        <NuxtPage />

        <div class="footer">
            <div class="footer-top">
                <div class="container footer-container">
    
    
                    <NuxtLink to="/" class="footer-items" @click="menu = false, basket = false, register = false, search = false">
                    <img src="../assets/images/home.svg" alt="svg" class="footer-items__img" />
                    </NuxtLink>
    
                    <NuxtLink to="/" class="footer-items" @click="search = true, menu = false, basket = false, register = false">
                    <img src="../assets/images/search2.svg" alt="svg" class="footer-items__img" />
                    </NuxtLink>
    
                    <NuxtLink to="/" class="footer-items" @click="menu = true, basket = false, register = false, search = false">
                    <img src="../assets/images/burger.svg" alt="svg" class="footer-items__img" />
                    </NuxtLink>
    
                    <NuxtLink to="/" class="footer-items" @click="basket = true, menu = false, register = false, search = false">
                    <img src="../assets/images/basket.svg" alt="svg" class="footer-items__img" />
                    </NuxtLink>
    
                    <NuxtLink to="/" class="footer-items" @click="register = true, basket = false, menu = false, search = false">
                    <img src="../assets/images/user.svg" alt="svg" class="footer-items__img" />
                    </NuxtLink>
    
    
                </div>
            </div>
        </div>



    </div>
</template>

<script setup>
const basket = ref(false)
const menu = ref(false)
const register = ref(false)
const search = ref(false)


</script>

<style lang="scss" scoped>

</style>