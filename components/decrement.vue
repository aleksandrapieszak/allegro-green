<template>
    <div>
        <button @click="decrement">
            usuń : {{ count }}
        </button>

    </div>
</template>

<script lang="ts" setup>
const count = ref(0)
const decrement = () => {
    count.value--
}
</script>