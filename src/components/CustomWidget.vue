<script setup lang="ts">
import { ref } from "vue";
interface WidgetConfig {
  // 根据实际业务补充字段
  [key: string]: unknown;
}

defineProps<{
  widget?: WidgetConfig;
}>();

const count = ref(0);
const increment = () => {
  count.value++;
};
</script>

<template>
  <div
    class="w-full h-full flex flex-col items-center justify-center p-4 bg-white rounded-xl relative overflow-hidden"
  >
    <div class="text-3xl mb-2">🧩</div>
    <div class="font-bold text-gray-700 text-sm mb-2">自定义组件</div>
    <div class="flex items-center gap-2">
      <button
        @click.stop="increment"
        class="px-3 py-1 bg-blue-50 text-blue-600 rounded-lg hover:bg-blue-100 transition-colors text-xs font-medium"
      >
        点击次数: {{ count }}
      </button>
    </div>
  </div>
</template>
