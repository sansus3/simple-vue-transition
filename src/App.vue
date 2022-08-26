<script>
import { ref } from 'vue';

export default {
  setup(){
    const show = ref(false);
    return {
      show,
    }
  }
}
</script>
<template>
  <div>
    <h1 class="text-center text-3xl font-bold underline">Suspense</h1>
    <button @click="show = !show" type="button">
      Click me {{show}}
    </button>
    <Transition>
      <p v-if="show">Transition 🙋‍♀️
      <div>
        &lt; Transition> is a <strong>built-in component</strong>: this means it is available in any component's template without having to register it. It can be used to apply enter and leave animations on elements or components passed to it via its default slot. The enter or leave can be triggered by one of the following:
          <ul>
            <li>Conditional rendering via v-if</li>
            <li>Conditional display via v-show</li>
            <li>Dynamic components toggling via the &lt;component> special element</li>
          </ul>
      </div>
      </p>
    </Transition>
  </div>
</template>
<style>
/* we will explain what these classes do next! */
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>