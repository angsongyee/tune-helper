<script lang="ts">
    let videoId: string = "fT8jkJAExX8"
    let videoUrl: string = "https://www.youtube.com/embed/" + videoId
    let playerReady: boolean =  true
</script>

<div>
    {#if playerReady}
        <iframe id="player" title="Youtube Embed" src={videoUrl}></iframe>
    {/if}
</div>

<style>
   iframe {
    height: 50vh;
    min-height: 200px;
    max-width: 80vw;
    aspect-ratio: 16 / 9;
   } 
</style>