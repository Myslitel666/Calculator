<script lang="ts">
  import { onMount } from "svelte";
  import { ButtonBox } from "svelte-elegant";
  import { Backspace } from "svelte-elegant/icons-elegant";

  let isInitialized = false;

  onMount(() => {
    isInitialized = true;
  });
</script>

<div class="page">
  <div class="buttons">
    <ButtonBox>,</ButtonBox>
    <ButtonBox>C</ButtonBox>
    <ButtonBox><Backspace /></ButtonBox>
    <ButtonBox>÷</ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox>1</ButtonBox>
    <ButtonBox>2</ButtonBox>
    <ButtonBox>3</ButtonBox>
    <ButtonBox>+</ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox>4</ButtonBox>
    <ButtonBox>5</ButtonBox>
    <ButtonBox>6</ButtonBox>
    <ButtonBox>-</ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox>7</ButtonBox>
    <ButtonBox>8</ButtonBox>
    <ButtonBox>9</ButtonBox>
    <ButtonBox>×</ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox>(</ButtonBox>
    <ButtonBox>0</ButtonBox>
    <ButtonBox>)</ButtonBox>
    <ButtonBox>=</ButtonBox>
  </div>
</div>

<style>
  .buttons {
    display: flex;
    gap: 10px;
  }

  .page {
    gap: 10px;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .timer {
    font-size: 48px;
    margin-top: 30px;
    margin-bottom: 30px;
  }

  .ms {
    font-size: 20px;
    margin-left: 5px;
  }
</style>
