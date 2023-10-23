<template class="overflow-hidden">
    <XyzTransition
        appear
        xyz="fade ease-in-out duration-10 delay-10"
    >
        <TresCanvas clear-color="#FEFBEB" preset="realistic" shadows>
            <TresPerspectiveCamera :position="[5, 5, 5]" :look-at="[0, 0, 0]" />
            <!-- <CameraControls v-bind="controlState" make-default /> -->
            <OrbitControls min-distance="5" max-distance="50" />
            <TresMesh ref="box_ref" :scale="1">
                <TresBoxGeometry :args="[1, 1, 1]" />
                <TresMeshNormalMaterial />
            </TresMesh>
        </TresCanvas>
    </XyzTransition>
</template>

<script setup>
/* eslint-disable */
import { TresCanvas, useRenderLoop } from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos'
import { ref } from 'vue'

const box_ref = ref(null);

const { onLoop } = useRenderLoop();

onLoop(() => {
    if(box_ref.value) {
        box_ref.value.rotation.y += 0.01;
        box_ref.value.rotation.x += 0.005;
    }
});
</script>

<style scoped>
</style>