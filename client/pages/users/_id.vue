<template>
  <header>
    <h1>{{ $route.params.id }}</h1>
  </header>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  validate({ params }) {
    // 라우트 매개변수 ID 값이 숫자인 경우만 허용
    return /^\d+$/.test(params.id);
  },
});
</script>
