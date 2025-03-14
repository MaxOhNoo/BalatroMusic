<script>
    import { booster, boss, main, planet, shop } from './music';

    const themes = [main, shop, booster, planet, boss];

    function stopall() {
        themes.forEach((theme) => theme.stop());
    }

    function playall() {
        for (const theme of themes) {
            console.log(`Playing ${theme._src} at ${new Date().getUTCMilliseconds()}`);
            theme.play();
        }
    }

    function log() {
        for (let i = 0; i < 1000; i++) {
            console.log(new Date().getUTCMilliseconds());
        }
    }
</script>

<div>
    <button onclick={() => main.play()}> Play Main Theme </button>
    <button onclick={() => shop.play()}> Play Shop Theme </button>
    <button onclick={() => booster.play()}> Play Booster Theme </button>
    <button onclick={() => planet.play()}> Play Planet Theme </button>
    <button onclick={() => boss.play()}> Play Boss Theme </button>
</div>

<div>
    <button onclick={() => playall()}> Play All </button>
    <button onclick={() => stopall()}> Stop Playing </button>
    <button onclick={() => log()}> Log </button>
</div>
