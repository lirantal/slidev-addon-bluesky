<!--
A simple wrapper for embedded Bluesky post

Usage:

<Bluesky id="at://did:plc:hnlvjno2m7l2kqllgum26bv2/app.bsky.feed.post/3lhr6jiuaqs25" />
-->

<script setup lang="ts">
import { isClient, useScriptTag } from '@vueuse/core'
import { ref } from 'vue'

const props = defineProps<{
    id: string
}>()

const tweet = ref<HTMLElement | null>()

if (isClient) {
    // @ts-expect-error Global variable
    if (!window?.bluesky?.scan) {
        useScriptTag('https://embed.bsky.app/static/embed.js',
        () => {}, { async: true })
    }
}
</script>

<template>
    <div class="w-full flex">
        <div ref="tweet" class="mx-auto w-140">
            <blockquote class="bluesky-embed" :data-bluesky-uri="props.id"> </blockquote>
        </div>
    </div>
</template>