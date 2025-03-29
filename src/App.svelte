<script lang="ts">
  import { onMount } from 'svelte';
  let dirs: string[] = [] 
  onMount(async () => { 
    const res = await fetch('../lib/img');
    dirs = await res.json()
    console.log(await res.json());
  })
  function getImagePath() {
    const index = Math.floor(Math.random() * dirs.length);
    const img = dirs[index]; console.log(img);
    return `../lib/img/${img}`;
  }
</script>

<!-- svelte-ignore a11y_img_redundant_alt -->
<img src={getImagePath()} alt="Random Image" />

<style>
</style>
