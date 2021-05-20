<script lang="ts">
  let toggle: boolean = true;
  let classes: string = 'text-red-500 text-sm';
</script>

<button on:click={() => (toggle = !toggle)}>Toggle [{toggle}]</button>

<p class={toggle ? 'bg-red-800 text-4xl' : 'bg-blue-800 text-6xl'}>toggleで動く</p>

<p class="text-blue-500">動く</p>
<p class="text-blue-400">動く</p>

<p class={'text-blue-300'}>動かない</p>
<p class={'text-blue-200'}>動かない</p>
<p class={`text-blue-100`}>動かない</p>

<p class={classes}>動かない</p>

<div class={toggle ? 'bg-blue-500' : 'bg-black'}>
  <p class="text-lg {toggle ? 'text-green-500' : 'text-white'}">動く</p>
</div>
