<template>
  <div class="home">
    <ModalContainer :isOpen="isOpen" msg="Welcome to myModal in  Vue.js" />
    <template>
      <button @click="open()">{{ isOpen ? 'close' : 'open' }} modal</button>
    </template>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import ModalContainer from '@/components/ModalContainer.vue';
import { Vue, Component } from 'vue-property-decorator';

@Component({
  components: { ModalContainer },
})
export default class Home extends Vue {
  isOpen = false;

  open(): void {
    this.isOpen = true;
  }
  close(): void {
    this.isOpen = false;
    console.log("!!!!");
    
  }
}
</script>
