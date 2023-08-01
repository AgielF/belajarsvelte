<script>
  import Belajar from "./belajar.svelte";
  let strHtml = "tag html dari gerak=<marquee>HTML<marquee/>";
  let count = 0;
  let arrayFactorial = [1];
  $: doubleCount = count * 2;

  function pencet() {
    count += 1;
    arrayFactorial = [...arrayFactorial, arrayFactorial.length + 1];
  }
</script>

<main>
  {@html strHtml}
  <div class="card">
    <Belajar />
  </div>
  <button on:click={pencet}>
    count={count}
  </button>
  <p>{doubleCount}</p>
  <p>{arrayFactorial}</p>
</main>
