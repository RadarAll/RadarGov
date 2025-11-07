<template>
    <button :class="['w-full font-semibold py-4 rounded-full transition-all duration-300 shadow-lg mt-5', variantClass]">
        <slot />
    </button>
</template>

<script setup>
defineProps(
    {
        variant: {
            type: String,
            default: 'primary'
        }
    }
)

const variantClass = {
    primary: 'bg-gradient-to-r from-green-800 to-green-600 hover:from-green-700 hover:to-green-500 text-white hover:shadow-green-500/10',
    secondary: '',
    error: '',
    success: '',
}[variant]

</script>