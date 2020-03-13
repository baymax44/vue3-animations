<template>
  <div class="about">
    <transition
      appear
      name="fade"
      @before-enter="beforeEnter"
      @enter="enter"
      @after-enter="afterEnter"
      @before-leave="beforeLeave"
      @leave="leave"
      @after-leave="afterLeave"
    >
      <h1 v-if="showTitle">About</h1>
    </transition>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam officia possimus delectus inventore quod quisquam culpa voluptas iusto, quae maiores quo dolorum, corporis laboriosam a dolore consequatur assumenda nam!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam officia possimus delectus inventore quod quisquam culpa voluptas iusto, quae maiores quo dolorum, corporis laboriosam a dolore consequatur assumenda nam!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam officia possimus delectus inventore quod quisquam culpa voluptas iusto, quae maiores quo dolorum, corporis laboriosam a dolore consequatur assumenda nam!</p>
  </div>
</template>

<script>
import { ref } from "vue"

export default {
  setup() {
    const showTitle = ref(true)

    const beforeEnter = () => {
      console.log("before enter")
    }
    const enter = () => {
      
    }
    const afterEnter = () => {
      
    }
    const beforeLeave = () => {
      
    }
    const leave = () => {
      
    }
    const afterLeave = () => {
      
    }

    return { showTitle, beforeEnter, enter, afterEnter, beforeLeave, leave, afterLeave }
  }
}
</script>

<style>
  .about {
    max-width: 600px;
    margin: 20px auto;
  }

  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 3s ease;
  }
</style>