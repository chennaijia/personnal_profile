<template>
    <div class="grid gap-4">
        <div class="w-full bg-white rounded-full border border-gray-300 px-6 shadow-md">
            <a
                v-if="link.href !== '-'"
                :href="link.href"
                :class="['px-1 py-2 rounded inline-block']"
                @click="link.onClick"
                >
                {{ link.href }}
            </a>
        </div>
    </div>
</template>
  
<script lang="ts">
  export default {
    name: 'link_url_component',
    props: {
        link: {
            type: Object,
            required: true,
            default: () => ({
                href: '-',
                onClick: () => {},
            })
        }
    }
  }
</script>
  