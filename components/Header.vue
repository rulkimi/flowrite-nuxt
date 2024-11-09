<script setup lang="ts">
const settings = useSettings();
</script>

<template>
  <Bounded as="header" class="!py-4 md:!py-6 lg:!py-8">
    <div class="flex gap-4 items-center justify-between flex-col sm:flex-row">
      <Logo />
      <nav>
        <ul class="flex">
          <li
            v-for="item of settings ?.data.navigation"
            :key="item.label ?? ''"
            class="p-4"
          >
            <PrismicLink :field="item.link">
              {{ item.label }}
            </PrismicLink>
          </li>
        </ul>
      </nav>
    </div>
  </Bounded>
</template>