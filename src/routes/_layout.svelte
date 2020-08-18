<script>
  import GoogleAnalytics from "../components/GoogleAnalytics.svelte";
</script>

<GoogleAnalytics />
<div>
  <main>
    <div id="homepage">
      <div class="container">
        <div class="small">
          <div class="page-title">
            <div>
              <a href=".">Home /</a>
              <a href="about">About</a>
            </div>
            <hr />
          </div>
        </div>
      </div>
      <slot />

      <!-- The link below is just for allow expost static post -->
      <a href="post"> </a>
    </div>
  </main>
</div>
