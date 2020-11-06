<template>
  <div class="wrapper">


    <div class="wrapper-content">
      <section>
        <div class="container">
          <button class="btn btnPrimary" @click="modalFirst = !modalFirst">Show first modal</button>
          <!-- first modal -->
          <modals 
            title="First Modal"
            v-show="modalFirst"
            @close="modalFirst = !modalFirst">
            
            <div slot="body">
              <p>Text</p>
              <button class="btn btnPrimary" @click="modalFirst = !modalFirst">Well Done</button>
            </div>

            </modals>
        </div>
      </section>


    </div>
  </div> 
</template>

<script>
import modals from '@/components/Modal.vue'

export default {
  components: { modals },
  data(){
    return {
      modalFirst: false
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
