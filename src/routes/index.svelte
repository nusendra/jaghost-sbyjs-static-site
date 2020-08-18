<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`post.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      })
  }
</script>

<script>
  export let posts;
</script>

<svelte:head>
  <title>JagHost - SbyJS</title>
</svelte:head>

<div class="container">
  <div class="small">
    <div class="column">
      <div>
        {#each posts as { slug, title }, index}
        <a href="post/{slug}">{title}</a>
        <br />
        {/each}
      </div>
    </div>
  </div>
</div>

<style>
.home-description {
  margin-top: -70px;
  margin-bottom: 40px;
}
</style>
