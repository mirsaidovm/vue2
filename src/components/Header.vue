<template>
    <header class="header">
        <transition name="header__notes" mode="out-in">
            <div class="header__notes" v-if="header">
                <h2 class="header__title">Заметки</h2>
                <button class="header__search" @click="header = false">
                    <i class="fa-solid fa-magnifying-glass"></i>
                </button>
            </div>
            <form class="header__form" v-else>
                <a href="#" class="back" @click="header = true">
                    <i class="fa-solid fa-arrow-left"></i>
                </a>
                <input type="text" placeholder="Поиск..." name="search" class="header__input">
                <a href="#" class="close" @click="header = true">
                    <i class="fa-solid fa-xmark"></i>
                </a>
            </form>
        </transition>
    </header>
</template>
<script>
export default {
    data(){
        return{
            header: true
        }
    }
}
</script>