<script lang="ts">
    import Background from "./lib/Background.svelte";
    import SoCool from "./lib/SoCool.svelte";
    import MediaQuery from "svelte-media-queries";
</script>

<main>
    <Background />
    <div class="so-cool-to-slider">
        <!-- {#each new Array(3).fill("") as a, i (i)}
            <SoCool speed={((i * 100) + 100)} />
        {/each} -->
        <MediaQuery query='(max-width: 480px)' let:matches>
            {#if matches}
                <SoCool speed={200} />
                <SoCool speed={400} />
            {:else}
                <SoCool speed={400} />
                <SoCool speed={200} />
                <SoCool speed={400} />
            {/if}
          </MediaQuery>
    </div>

    <div class="so-cool-to-see">
        <span>ทำด้วยความเท่ : โครตเท่สตูดิโอ</span>
        <img src="favicon.ico" width="20" height="20" alt="โครตเท่สตูดิโอไอคอนนิค">
    </div>
</main>

<style lang="scss">
    main {
        // overflow: hidden;
        // width: 100vw;
        // height: 100vh;
        // display: flex;
        // justify-content: center;
        // align-items: center;

        .so-cool-to-slider {
            overflow: hidden;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            // row-gap: 2rem;
        }

        .so-cool-to-see {
            position: absolute;
            top: 1rem;
            left: 1rem;
            background-color: black;
            padding: 10px 2rem 8px 2rem;
            border-radius: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            gap: 6px;
        }
    }
</style>
