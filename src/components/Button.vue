<script lang="ts" setup>
defineProps({
    small: {
        type: Boolean,
        default: false
    },
    color: {
        type: String,
        default: "#f46663"
    }
});
</script>

<template>
    <button :class="{btn: true, 'btn--small': small}" :style="{backgroundColor: color}">
        <slot></slot>
    </button>
</template>

<style scoped>
.btn {
    padding: 16px 32px;
    border-radius: 48px;
}

.btn--small {
    padding: 12px 24px;
}
</style>