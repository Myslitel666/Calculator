<script lang="ts">
  import { onMount } from "svelte";
  import { ButtonBox, TextField } from "svelte-elegant";
  import { Backspace } from "svelte-elegant/icons-elegant";

  let isInitialized = false;
  let buttonBoxSize = "85px";

  onMount(() => {
    isInitialized = true;
  });
</script>

<div class="page">
  <TextField width="369px" />
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>,</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>C</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>
      <Backspace size="45px" />
    </ButtonBox>
    <ButtonBox fontSize="38px" width={buttonBoxSize} height={buttonBoxSize}>
      ÷
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>1</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>2</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>3</ButtonBox>
    <ButtonBox fontSize="38px" width={buttonBoxSize} height={buttonBoxSize}>
      +
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>4</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>5</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>6</ButtonBox>
    <ButtonBox fontSize="38px" width={buttonBoxSize} height={buttonBoxSize}>
      -
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>7</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>8</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>9</ButtonBox>
    <ButtonBox fontSize="38px" width={buttonBoxSize} height={buttonBoxSize}>
      ×
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>(</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>0</ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>)</ButtonBox>
    <ButtonBox
      isPrimary
      fontSize="38px"
      width={buttonBoxSize}
      height={buttonBoxSize}
    >
      =
    </ButtonBox>
  </div>
</div>

<style>
  .buttons {
    display: flex;
    gap: 10px;
  }

  .page {
    margin-top: 10px;
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
