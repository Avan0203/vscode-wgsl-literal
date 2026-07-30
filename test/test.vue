<template>
    <div>
        <h1>Hello World</h1>
    </div>
</template>

<script setup>
const props = defineProps({
    name: {
        type: String,
        required: true
    }
})

const shader = /* wgsl */ `
    @vertex fn vs(
        @builtin(vertex_index) vertexIndex : u32
    ) -> @builtin(position) vec4f {
        return vec4f(0.0, 0.0, 0.0, 1.0);
    }
`;
</script>


