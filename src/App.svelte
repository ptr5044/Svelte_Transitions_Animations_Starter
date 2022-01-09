<script>
  import { imageData } from "./Images";
</script>

<section>
  {#each imageData as image, i}
    <div class="card__wrapper">
      <img src={image.url} alt="card" />
    </div>
  {/each}
</section>

<style>
  section {
    display: grid;
    max-width: 100vw;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    grid-gap: 1rem;
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    aspect-ratio: 1 / 1.5;
    border-radius: 15px;
  }
</style>
