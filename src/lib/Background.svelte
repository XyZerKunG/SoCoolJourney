<script lang="ts">
    import SoItIsBackground from "../assets/SoItsBackground.png"
</script>

<div class="bg" style="background-image: url({SoItIsBackground});" />

<style>
    .bg {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        overflow: hidden;
        filter: brightness(0.7) contrast(0.75) saturate(2) brightness(1.5);
        background-color: #4cc9df;
        background-size: cover;
        background-position: center;
    }
</style>