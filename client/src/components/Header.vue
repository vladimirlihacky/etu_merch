<script setup>
import Logo from "../assets/icons/logo.svg"
import Search from "../assets/icons/search.svg"
import Accessories from "../assets/pictures/accessories.png"
import Clothes from "../assets/pictures/clothes.png"
import Other from "../assets/pictures/other.png"
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
            <div class="categories">
                <a href="" class="category">
                    <img :src="Clothes" class="category-bg" />
                    Одежда
                </a>
                <a href="" class="category">
                    <img :src="Clothes" class="category-bg" />
                    Одежда
                </a>
                <a href="" class="category">
                    <img :src="Clothes" class="category-bg" />
                    Одежда
                </a>
            </div>
        </div>
    </header>
</template>

<style scoped>
header {
    padding: 0 40px 30px 40px;
    background: rgba(53, 131, 247, 0.20);
    display: flex;
    flex-direction: column;
    gap: 30px;
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

.categories {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    width: 100%;
}

.category {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    height: 80px;
    padding: 0px 30px 0 40px;
    color: white;
    text-decoration: none;
}

.category-bg {
    object-fit: cover;
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -1;
    left: 0;
    top: 0;
}

.category:hover {
    
}
</style>