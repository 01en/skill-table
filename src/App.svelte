<script>
  import SvelteTable from "svelte-table";
  export let name;
  const rows = [
    { user: "1coin", tech: "React", level: "○" },
    { user: "1coin", tech: "Svelth", level: "x" }
  ];
  const columns = [
    {
      key: "user",
      title: "user",
      value: v => v.user,
      sortable: true,
      class: "cell"
    },
    {
      key: "tech",
      title: "tech",
      value: v => v.tech,
      sortable: true
    },
    {
      key: "level",
      title: "level",
      value: v => v.level,
      sortable: true
    }
  ];
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  cell {
    text-align: center;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
</main>

<SvelteTable {columns} {rows} />
