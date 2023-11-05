<script setup>
import Logo from "../assets/icons/logo.svg"
import Search from "../assets/icons/search.svg"
import Bin from "../assets/icons/bin.svg"
import Umbrella from "../assets/pictures/umbrella.png"
</script>

<template>
    <header>
        <div class="top-nav">
            <div class="logo">
                <img :src="Logo" alt="">
            </div>
            <div class="search">
                <button class="search-btn">
                    <img :src="Search" alt="">
                </button>

                <input type="text" class="search-input">
            </div>
            <div class="nav-links">
                <a href="" class="nav-link">Каталог</a>
                <a href="" class="nav-link">Корзина</a>
            </div>
        </div>
        <!-- Вот bottom-nav будет меняться в зависимости от того, что в компонент передаем -->
        <div class="bottom-nav">
            <a href="" class="return">
                <span>На главную</span>
            </a>
        </div>
    </header>
    <body>
        <span class="cart-text">Корзина</span>
        <div class="items">
            <div class="item">
                <div class="top-item">
                    <img :src="Umbrella" alt="">
                </div>
                <div class="low-item">
                    <span class="price">1200p</span>
                    <span class="nametag">Электромагический зонт</span>
                    <div class="functionality">
                        <div class="item-count">
                            <span class="minus">-</span>
                            <span class="count">1 шт</span>
                            <span class="plus">+</span>
                        </div>
                        <div class="bin">
                            <img :src="Bin" alt="">
                        </div>
                    </div>
                </div>
            </div>
            <div class="item">
                <div class="top-item">
                    <img :src="Umbrella" alt="">
                </div>
                <div class="low-item">
                    <span class="price">1200p</span>
                    <span class="nametag">Электромагический зонт</span>
                    <div class="functionality">
                        <div class="item-count">
                            <span class="minus">-</span>
                            <span class="count">1 шт</span>
                            <span class="plus">+</span>
                        </div>
                        <div class="bin">
                            <img :src="Bin" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </body>
</template>

<style scoped>
header {
    padding: 0 40px 30px 40px;
    background: rgba(53, 131, 247, 0.20);
    display: flex;
    flex-direction: column;
    gap: 30px;
}

body {
    width: 100%; 
    height: 100%;
    padding: 30px 40px 30px 40px;
    background: rgba(53, 131, 247, 0.10);
    display: flex;
    flex-direction: column;
    gap: 50px;
}

.top-nav {
    height: 90px;
    display: flex;
    justify-content: space-between;
    gap: 50px;
    align-items: center;
}

.search {
    height: 60px;
    border-radius: 15px;
    background: rgba(53, 131, 247, 0.10);
    display: flex;
    align-items: center;
    padding: 10px 15px;
    gap: 10px;
    width: 100%;
}

.search-btn {
    background: none;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
}

.search-input {
    background: none;
    border: none;
    width: 100%;
}

.search-input:focus {
    outline: none;
}

.nav-links {
    display: flex;
    gap: 30px;
}

.nav-link {
    color: #000c;
    text-decoration: none;
}

.return {
    width: fit-content; 
    height: 100%; 
    padding: 15px 20px 15px 15px;
    background: #353DF7; 
    border-radius: 15px; 
    overflow: hidden; 
    justify-content: flex-start; 
    align-items: center; 
    gap: 10px; 
    display: flex;

    color: white; 
    font-size: 20px; 
    font-family: TT Norms; 
    font-weight: 500; 
    word-wrap: break-word;
    text-decoration: none;
}

.cart-text {
    color: rgba(0, 0, 0, 0.80); 
    font-size: 32px; 
    font-family: TT Norms; 
    font-weight: 700; 
    word-wrap: break-word;
}

.items {
    width: 100%; 
    height: 100%; 
    justify-content: flex-start; 
    align-items: center; 
    gap: 20px; 
    display: flex;
}

.item {
    width: fit-content; 
    height: 100%; 
    background: rgba(0, 0, 0, 0.05); 
    border-radius: 15px; 
    overflow: hidden; 
    border: 1px solid; 
    flex-direction: column; 
    justify-content: flex-start; 
    align-items: flex-start; 
    display: flex;
}

.top-item {
    width: 100%; 
    height: 100%; 
    background: rgba(0, 0, 0, 0.05); 
    border-radius: 15px; 
    overflow: hidden; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; 
    display: flex;
}

.low-item {
    width: 100%; 
    height: 100%; 
    padding: 20px; 
    flex-direction: column; 
    justify-content: flex-start; 
    align-items: flex-start; 
    display: flex;
}

.price {
    color: #353DF7; 
    font-size: 25px; 
    font-family: TT Norms; 
    font-weight: 700; 
    word-wrap: break-word;
}

.nametag {
    color: rgba(0, 0, 0, 0.80); 
    font-size: 20px; 
    font-family: TT Norms; 
    font-weight: 500; 
    word-wrap: break-word;
}

.functionality {
    width: 100%; 
    height: 100%; 
    padding-top: 10px; 
    justify-content: space-between; 
    align-items: center; 
    display: flex;
}

.item-count {
    width: 100%; 
    height: 100%; 
    justify-content: flex-start; 
    align-items: center; 
    gap: 15px; 
    display: flex;
}

.minus {
    width: 40px; 
    height: 40px;
    padding: 0 10px 4px 10px; 
    background: rgba(0, 0, 0, 0.05); 
    border-radius: 8px; 
    overflow: hidden; 
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; display: flex;

    color: rgba(0, 0, 0, 0.60); 
    font-size: 32px; 
    font-family: TT Norms; 
    font-weight: 700; 
    line-height: 32px; 
    word-wrap: break-word;
}

.count {
    color: rgba(0, 0, 0, 0.60); 
    font-size: 20px; 
    font-family: TT Norms; 
    font-weight: 500; 
    line-height: 20px; 
    word-wrap: break-word;
}

.plus {
    width: 40px; 
    height: 40px; 
    padding: 0 10px 4px 10px;
    background: rgba(0, 0, 0, 0.05); 
    border-radius: 8px; 
    overflow: hidden; 
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; 
    display: flex;

    color: rgba(0, 0, 0, 0.60); 
    font-size: 32px; 
    font-family: TT Norms; 
    font-weight: 700; 
    line-height: 32px; 
    word-wrap: break-word;
}

.bin {
    width: 40px; 
    height: 40px;
    padding: 0 10px 0 10px; 
    background: rgba(0, 0, 0, 0.05); 
    border-radius: 8px; 
    overflow: hidden; 
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; 
    display: flex;
}

</style>