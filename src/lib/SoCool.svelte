<script lang="ts">
    import { onMount } from "svelte";
    import SoCool from "../assets/SoCool.png";
    export let speed = 1;
    let y = 0;

    function a() {
        y += speed;
    }

    onMount(() => {
        const i = setInterval(() => {
            a()
        }, 5000);
        return () => {
            clearInterval(i);
        };
    });
</script>

<div class="so-cool">
    <div
        class="so-cool-text"
        style="background-image: url({SoCool});background-position: 0 {y*-1}px;"
    />
</div>

<style lang="scss">
    .so-cool {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        color: white;
        user-select: none;
        width: 100%;
        height: 100%;
    }
    .so-cool-text {
        position: relative;
        font-size: 250px;
        max-width: 600px;
        opacity: 0.5;
        width: 100%;
        height: 100%;
        background-size: contain;

        transition: background-position 4s;
    }
</style>
