<template>
    <div class="notes">
        <div class="container">
            <div class="notes__nav">
                <h3 class="notes__title">Все заметки</h3>
                <button class="notes__checker" @click="grid = !grid">
                    <i class="fa-solid fa-list" v-if="grid"></i>
                    <i class="fa-solid fa-table-cells" v-else></i>
                    <span>{{grid ? 'Список' : 'Сетка'}}</span>
                </button>
            </div>
            <transition-group tag="div" class="notes__grid" name="notes" :class="{column: !grid}">
                <OneNote/>
            </transition-group>
        </div>
    </div>
</template>
<script>
import OneNote from './OneNote.vue'
export default {
    components: {OneNote},
    data(){
        return{
            grid: true
        }
    }
}
</script>ё