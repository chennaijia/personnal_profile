<template>
    <div class="grid gap-4 px-1">
        <div class="space-y-6">
            <div class="flex items-center justify-between">
                <label class="block text-sm font-medium leading-6 text-gray-600">公開連結</label>
            </div>

            <div class="grid gap-4">
                <div 
                    v-for= "(link, index) in links" 
                    :key="index" 
                    class="w-full bg-white rounded-full border border-gray-300 px-6 shadow-md"
                >
                    <a
                        :href="link.href"
                        class="px-1 py-2 rounded inline-block"
                        @click="link.onClick"
                    >
                        {{ link.href }}
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script lang="ts">
  export default {
    name: 'link_component',
    props: {
        first_link: {
            type: Object,
            required: true,
            default: () => ({
                href: '-',
                onClick: () => {},
            })
        },
        second_link: {
            type: Object,
            required: true,
            default: () => ({
                href: '-',
                onClick: () => {},
            })
        },
        third_link: {
            type: Object,
            required: true,
            default: () => ({
                href: '-',
                onClick: () => {},
            })
        },links: {
            type: Array,
            required: true,
            default: () => [
                { href: '-', onClick: () => {} },
                { href: '-', onClick: () => {} },
                { href: '-', onClick: () => {} },
            ],
        },
    }
  }
</script>
  