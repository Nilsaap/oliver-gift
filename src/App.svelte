<script lang="ts">
  import json from './lib/imgs.json';
  let dir: string;
  const index = Math.floor(Math.random() * json.length);
  dir = json[index];
  console.log(dir);
</script>

<div>
  <img src={`/img/${dir}`} alt="Random Image" />

</div>

<style>
  div {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: black;
  }
  html, body, root{
    padding: 0;
    margin: 0;
    width: 100%;
  }
</style>
