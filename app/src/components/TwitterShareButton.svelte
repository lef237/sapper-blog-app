<script lang="ts">
  import TwitterIcon from "./Icons/Twitter.svelte";
  export let url: string;
  export let text: string;

  $: escapedText = encodeURIComponent(text);
</script>

<a
  href={`https://x.com/share?url=${url}&text=${escapedText}}`}
  target="_blank"
  rel="noopener noreferrer"
>
  <span class="sr-only">Xで共有</span>
  <TwitterIcon className="h-6 w-6 text-black dark:text-white" />
</a>
