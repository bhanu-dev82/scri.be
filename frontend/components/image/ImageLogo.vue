<!-- SPDX-License-Identifier: AGPL-3.0-or-later -->
<template>
  <a class="focus-brand group rounded-xl" :href="imageLink" target="_blank">
    <div
      class="bg-layer-1 relative z-0 h-[200px] w-[200px] rounded-xl group-hover:bg-highlight group-hover:fill-primary-text lg:h-[250px] lg:w-[250px]"
    >
      <div
        class="z-1 absolute inset-0 flex items-center justify-center overflow-clip"
      >
        <div v-if="imageName == 'WikimediaFoundation'">
          <LogoWikimediaFoundation
            class="h-[200px] w-[200px] scale-[0.7] rounded-md group-hover:fill-primary-text lg:h-[250px] lg:w-[250px] lg:rounded-lg"
          />
          <span class="sr-only">Wikimedia Foundation</span>
        </div>
        <div v-if="imageName == 'WikimediaDeutschland'">
          <LogoWikimediaDeutschland
            class="h-[200px] w-[200px] group-hover:fill-primary-text lg:h-[250px] lg:w-[250px]"
          />
          <span class="sr-only">Wikimedia Deutschland</span>
        </div>
      </div>
    </div>
  </a>
</template>

<script setup lang="ts">
defineProps<{
  imageName?: string;
  imageLink?: string;
}>();
</script>
