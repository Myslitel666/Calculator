<script lang="ts">
  import { onMount } from "svelte";
  import { ButtonBox, TextField } from "svelte-elegant";
  import { Backspace } from "svelte-elegant/icons-elegant";
  import { themeStore } from "svelte-elegant/stores";

  let isInitialized = false;
  let buttonBoxSize = "85px";
  let expression = "0";

  function inputNumber(number: string) {
    if (expression === "0") {
      expression = number;
    } else {
      expression += number;
    }
  }

  function backspace() {
    if (expression.length === 1) {
      expression = "0";
    } else {
      expression = expression.slice(0, -1);
    }
  }

  onMount(() => {
    isInitialized = true;
  });
</script>

<div class="page">
  <TextField
    bind:value={expression}
    label="Expression"
    textAlign="right"
    fontSize="20px"
    width="369px"
  />
  <div class="buttons">
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      color={$themeStore.palette.primary}
      onClick={() => {
        expression = "0";
      }}
    >
      C
    </ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize} onClick={backspace}>
      <Backspace fill={$themeStore.palette.primary} size="45px" />
    </ButtonBox>
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>,</ButtonBox>

    <ButtonBox
      fontSize="38px"
      width={buttonBoxSize}
      height={buttonBoxSize}
      color={$themeStore.palette.primary}
    >
      ÷
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("1");
      }}>1</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("2");
      }}>2</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("3");
      }}>3</ButtonBox
    >
    <ButtonBox
      fontSize="38px"
      width={buttonBoxSize}
      height={buttonBoxSize}
      color={$themeStore.palette.primary}
    >
      +
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("4");
      }}>4</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("5");
      }}>5</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("6");
      }}>6</ButtonBox
    >
    <ButtonBox
      fontSize="38px"
      width={buttonBoxSize}
      height={buttonBoxSize}
      color={$themeStore.palette.primary}
    >
      -
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("7");
      }}>7</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("8");
      }}>8</ButtonBox
    >
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("9");
      }}>9</ButtonBox
    >
    <ButtonBox
      fontSize="38px"
      width={buttonBoxSize}
      height={buttonBoxSize}
      color={$themeStore.palette.primary}
    >
      ×
    </ButtonBox>
  </div>
  <div class="buttons">
    <ButtonBox width={buttonBoxSize} height={buttonBoxSize}>(</ButtonBox>
    <ButtonBox
      width={buttonBoxSize}
      height={buttonBoxSize}
      onClick={() => {
        inputNumber("0");
      }}>0</ButtonBox
    >
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
