
<template>
  <div>
    <p class="text-4xl">
      <Icon class="iconify inline-block" icon="carbon:pedestrian" />
    </p>
    <p>
      {{ t('intro.hi', {name}) }}
    </p>
    <p class="text-sm opacity-50">
      <em>{{ t('intro.dynamic-route') }}</em>
    </p>

    <div>
      <button
        class="btn m-3 text-sm mt-8"
        @click="router.back()"
      >
        {{ t('button.back') }}
      </button>
    </div>
  </div>
</template>

<script setup lang='ts'>
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'
import { defineProps } from 'vue'

const props = defineProps({
  name: {
    type: String,
    require: true,
  },
})

const router = useRouter()
const { t } = useI18n()
</script>
