<script>
  export let data
</script>

<div
  class="embed-container rounded-box"
  style={`view-transition-name: ${data.video.id.replace(/[^a-zA-Z]/g, "")}-img`}>
  <iframe
    title={data.videos.find((video) => video.id == data.video.id).snippet.title}
    src={`https://www.youtube.com/embed/${data.video.id}`}
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>
<div class="h-10" />
<h1 class="text-3xl font-bold">
  {data.videos.find((video) => video.id == data.video.id).snippet.title}
</h1>
<div class="h-10" />
<div class="text-base-content/60 bg-base-200 rounded-box p-6">
  <p class="mx-auto max-w-2xl text-sm">
    {data.videos.find((video) => video.id == data.video.id).snippet.description}
  </p>
</div>

<style>
  .embed-container {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    max-width: 100%;
  }
  .embed-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
</style>
