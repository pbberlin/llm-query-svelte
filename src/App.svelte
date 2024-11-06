<script lang="ts">

  
  //  /vite.svg  is in  [root]/public
  import viteLogo   from      '/vite.svg'

  import svelteLogo from      './assets/svelte.svg'
  import Counter    from      './lib/Counter.svelte'
  import ChatCompletion from  './lib/ChatCompletion.svelte'


  let modelsVal  : string[] = [ "gpt-4o", "gpt-4" ];
  let promptMsgA : string   = `Who was Sheakespeare?
      Was he a noble man from the court?
      Use the following json format for your response:

      {{
          "agreement":        "<agrees/disagrees/neutral>",
          "alignment":         <percentage_score>
          "textual_analysis":  <text>
      }}
  `;

</script>

<main>

  <h4> &nbsp;Vite   &nbsp;  +  &nbsp; &nbsp;  Svelte</h4>
  <div>
    <a href="https://vite.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo}     class="logo vite"       alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo}   class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>

  <div class="card">
    <Counter />
  </div>


  <div style="text-align:left;">

    <ChatCompletion 
      promptMsg={promptMsgA}
      models={modelsVal}
    />
  </div>




</main>

<style>
  .logo {
    height: 6em;
    height: 3em;
    padding: 1.5em;
    padding: 0.5em;
    will-change: filter;
    transition:  filter 300ms;
  }
  .logo.vite:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
</style>


