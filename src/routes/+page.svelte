<script>
    import { boss, main, planet, shop, tarot } from './music';

    const themes = [main, shop, tarot, planet, boss];

    function stopall() {
        themes.forEach((theme) => theme.stop());
    }

    function playall() {
        themes.forEach((theme) => theme.play());
    }
</script>

<div>
    <button onclick={() => main.play()}> Play Main Theme </button>
    <button onclick={() => shop.play()}> Play Shop Theme </button>
    <button onclick={() => tarot.play()}> Play Tarot Theme </button>
    <button onclick={() => planet.play()}> Play Planet Theme </button>
    <button onclick={() => boss.play()}> Play Boss Theme </button>
</div>

<div>
    <button onclick={() => playall()}> Play All </button>
    <button onclick={() => stopall()}> Stop Playing </button>
</div>
