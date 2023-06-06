<script setup lang="ts">
import { ref, onMounted } from 'vue'
import TCPlayer from 'tcplayer.js';
import 'tcplayer.js/dist/tcplayer.min.css';

const myRef = ref(null);

onMounted(() => {

  const player = new TCPlayer(myRef.value, {
    fileID: '243791576943072647',
    appID: '1306264703',
    psign: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhcHBJZCI6MTMwNjI2NDcwMywiZmlsZUlkIjoiMjQzNzkxNTc2OTQzMDcyNjQ3IiwiY3VycmVudFRpbWVTdGFtcCI6MTY3MDQ2OTk3MSwiY29udGVudEluZm8iOnsiYXVkaW9WaWRlb1R5cGUiOiJQcm90ZWN0ZWRBZGFwdGl2ZSIsImRybUFkYXB0aXZlSW5mbyI6eyJwcml2YXRlRW5jcnlwdGlvbkRlZmluaXRpb24iOjEyfX0sInVybEFjY2Vzc0luZm8iOnsiZG9tYWluIjoiMTMwNjI2NDcwMy52b2QyLm15cWNsb3VkLmNvbSIsInNjaGVtZSI6IkhUVFBTIn19.FOcmChHfrGY9tYCDn20MSQi-IqvQ9U_U6qLNgx9MhLg',
    
  });

  player.on('loadedmetadata', () => {
    console.log('loadedmetadata');
  });

})
</script>

<template>
  <main>
    <video ref="myRef" id="player-container-id" width="414" height="270" preload="auto" playsinline webkit-playsinline>
    </video>
  </main>
</template>
