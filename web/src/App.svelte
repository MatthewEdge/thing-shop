<script>
  import Header from "./Header.svelte"
  import Item from "./Item.svelte"
</script>

<div class="app">
  <header>
    <Header />
  </header>

  <main>
    <ul class="items">
      <li>
        <Item
          name={"Thing 1"}
          description={"Thing One"}
          imgSrc={"https://bulma.io/images/placeholders/1280x960.png"}
        />
      </li>
      <li>
        <Item
          name={"Thing 2"}
          description={"Thing Two"}
          imgSrc={"https://bulma.io/images/placeholders/1280x960.png"}
        />
      </li>
      <li>
        <Item
          name={"Thing 3"}
          description={"Thing Three"}
          imgSrc={"https://bulma.io/images/placeholders/1280x960.png"}
        />
      </li>
      <li>
        <Item
          name={"Thing 4"}
          description={"Thing Four"}
          imgSrc={"https://bulma.io/images/placeholders/1280x960.png"}
        />
      </li>
    </ul>
  </main>

  <footer>
    <p>Copyright &copy; 2020 MedgeLabs</p>
  </footer>
</div>

<style>
  .app {
    height: 100%;
    display: grid;
    grid-template-areas: "header"
                         "main"
                         "footer";
    grid-template-rows: 50px 1fr 30px;
    background-color: #f8f8ff;
  }

  header {
    grid-area: header;
    background-color: #353535;
    color: #ffffff;
  }

	main {
    grid-area: main;
    margin: 0;
    padding: 10px;
	}

  ul.items { padding: 0; }

  .items {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    grid-gap: 10px;
  }

  .items > li {
    list-style-type: none;
  }

  footer {
    grid-area: footer;
    background-color: #353535;
    color: #ffffff;
    text-align: center;

    /* To center content */
    display: grid;
    align-content: center;
  }
</style>
