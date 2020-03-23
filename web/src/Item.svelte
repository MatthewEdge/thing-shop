<script>
  export let name;
  export let description;
  export let price = "$12.00";
  /* export let imgSrc; */
</script>

<div class="item">
  <div class="item-image">
    <img src="https://bulma.io/images/placeholders/96x96.png" alt={name}/>
  </div>
  <div class="item-content">
    <div class="content">
      <p class="name">{name}</p>
      <p class="description">{description}</p>
      <p class="price">{price}</p>
    </div>
  </div>
</div>

<style>
  .item {
    display: grid;
    grid-template-areas: "img name"
                         "img description"
                         "img price";

    background-color: white;
    box-shadow: 0 0.5em 1em -0.125em rgba(10, 10, 10, 0.1), 0 0px 0 1px rgba(10, 10, 10, 0.02);
    color: #4a4a4a;
    max-width: 100%;
    position: relative;
  }

  .item-image {
    grid-area: img;
    padding: 1em;
  }

  .item-image > img {
    width: 100%;
    height: 100%;
    border: 1px solid #000;
  }

  .item-content {
    background-color: transparent;
    padding: 1.5rem;
  }
</style>
