<script setup>
import Logo from "../assets/icons/logo.svg"
import Search from "../assets/icons/search.svg"
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
                <span>K выбору одежды</span>
            </a>
        </div>
    </header>
    <body>
        <div class="item-frame">
            <div class="left-part">
                <img :src="Umbrella" alt="">
            </div>
            <div class="right-part">
                    <span class="item-name">Электромагический зонт</span>
                    <span class="description">Невероятно крутой зонт который прекрасно защитит вас от мрачной сырости и ужасной питерской погоды</span>
                    <span class="price">1886р</span>
                    <div class="right-buttons">
                        <a href="" class="buy">Купить</a>
                        <a href="" class="add">В корзину</a>
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
    padding: 10px 0 0 20px;
    background: rgba(53, 131, 247, 0.10);
    display: flex;
    flex-direction: row;
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

.item-frame {
    padding: 20px;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 50px;
}

.left-part {
    width: 100%;
    height: 100%;
    padding: 60px;
    background: rgba(0, 0, 0, 0.05);
    border-radius: 15px; 
    overflow: hidden; 
    justify-content: center; 
    align-items: center; 
    display: flex;
}

.right-part {
    width: 100%;
    height: 100%;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 30px;
    display: flex;
}

.item-name {
    color: rgba(0, 0, 0, 0.80);
    font-size: 32px; font-family: TT Norms;
    font-weight: 700;
    word-wrap: break-word;
}

.description {
    width: 100%;
    color: rgba(0, 0, 0, 0.60);
    font-size: 20px;
    font-family: TT Norms;
    font-weight: 500;
    word-wrap: break-word;
}

.price {
    color: #3B43FF;
    font-size: 32px;
    font-family: TT Norms;
    font-weight: 700;
    word-wrap: break-word;
}

.right-buttons {
    width: 100%;
    height: 100%;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 11px;
    display: inline-flex;
}

.buy {
    width: fit-content; 
    height: 100%; 
    padding: 15px 25px 15px 25px; 
    background: #353DF7; 
    border-radius: 15px; 
    overflow: hidden; 
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; 
    display: flex;

    color: white; 
    font-size: 25px; 
    font-family: TT Norms; 
    font-weight: 500; 
    word-wrap: break-word;
    text-decoration: none;
}

.add {
    width: fit-content; 
    height: 100%; 
    padding: 15px 25px 15px 25px;
    background: rgba(53.50, 61.23, 246.91, 0.10); 
    border-radius: 15px; 
    overflow: hidden; 
    flex-direction: column; 
    justify-content: center; 
    align-items: center; 
    gap: 10px; 
    display: flex;

    color: #353DF7; 
    font-size: 25px; 
    font-family: TT Norms; 
    font-weight: 500; 
    word-wrap: break-word;
    text-decoration: none;
}

</style>