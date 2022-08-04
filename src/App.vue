<template>
  <Header/>
  <Notes/>
  <a href="" class="add__note">
    <i class="fa-solid fa-pencil"></i>
  </a>
</template>
<script>
  import '@/assets/styles/main.scss'
  import Header from './components/Header.vue'
  import Notes from './components/Notes.vue'
export default {
  components: {Header, Notes}
}
</script>