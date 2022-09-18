<script lang="ts">
    type player = "local" | "youtube"
    let playerType: player = "youtube";

</script>

<div class="container">
    <div class="merge-btn">
        <button class:selected="{playerType == "local"}" 
                on:click={()=> playerType = "local"} class="btn-left">
            Load audio file
        </button>
        <button class:selected="{playerType == "youtube"}" 
                on:click={()=> playerType = "youtube"} class="btn-right">
            Load Youtube Video
        </button>
    </div>
    <div>
        {#if playerType == "youtube"}
        <input placeholder="Youtube URL">
        {:else}
        <!--TODO: filepicker-->
        {/if}

    </div>
</div>


<style>
    .container {
        padding: 1em;
    }

    .container div {
        display: flex;
    }

    .merge-btn {
        width: 100%;
        margin: 0;
    }
    .merge-btn button {
        height: 3.5em;
        flex-grow: 1;
    }
    .btn-left {
        border-top-right-radius: 0;
        border-bottom-right-radius: 0;
    }

    .btn-right {
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
    }
    button.selected {
        background-color: #525252;
    }

    input {
        flex-grow: 1;
        height: 2.5em;
    }
</style>