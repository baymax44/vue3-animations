<template>
  <div class="home">
    <transition name="toast">
      <Toast v-if="showToast" />
    </transition>
    <Todos @badValue="triggerToast" />
  </div>
</template>

<script>
import { ref } from 'vue'
import Toast from '../components/Toast'
import Todos from '../components/Todos'

export default {
  components: { Toast, Todos },
  setup() {
    const showToast = ref(false)

    const triggerToast = () => {
      showToast.value = true;
      setTimeout(() => showToast.value = false, 3000)
    }

    return { showToast, triggerToast }
  }
}
</script>

<style>
.toast-enter-from {
  opacity: 0;
  transform: translateY(-60px);
}
.toast-enter-active,
.toast-leave-active {
  transition: all 1s ease;
}
.toast-leave-to {
  opacity: 0;
  transform: translateY(-60px);
}
</style>