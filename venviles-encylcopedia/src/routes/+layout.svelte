<script>
  import { page } from "$app/stores";
  import "$lib/style/styles.css";
</script>

<head
  ><link
    href="https://fonts.googleapis.com/css?family=Charm"
    rel="stylesheet"
  />
</head>

<div class="app">
  <nav>
    <li aria-current={$page.url.pathname === "/" ? "page" : undefined}>
      <a href="/">Encyclopédie</a>
    </li>
    <li aria-current={$page.url.pathname === "/about" ? "page" : undefined}>
      <a href="/about">???</a>
    </li>
    <li
      aria-current={$page.url.pathname.startsWith("/sverdle")
        ? "page"
        : undefined}
    >
      <a href="/sverdle">Personnage</a>
    </li>
  </nav>

  <main>
    <aside class="left-sider">
      <ul>
        <li>
          <a href="/nations">Nations</a>
          <input type="checkbox" style="display : none" id="cb" /><label
            for="cb"
            id="nation-folder"
          />
          <ul class="hider">
            <li><a href="/nations/alastia">Alastia</a></li>
            <li><a href="/nations/almotumia">Almotumia</a></li>
            <li><a href="/nations/andominchia">Andominchia</a></li>
            <li><a href="/nations/bozane">Bozane</a></li>
            <li><a href="/nations/castia">Castia</a></li>
            <li><a href="/nations/darenia">Darenia</a></li>
            <li><a href="/nations/eltala">Eltala</a></li>
            <li><a href="/nations/estrieria">Estrieria</a></li>
            <li><a href="/nations/euturia">Euturia</a></li>
            <li><a href="/nations/foniamia">Foniamia</a></li>
            <li><a href="/nations/kirsmilya">Kirsmilya</a></li>
            <li><a href="/nations/kohtilu">Kohtilu</a></li>
            <li><a href="/nations/martus">Martus</a></li>
            <li><a href="/nations/mustila">Mustila</a></li>
            <li><a href="/nations/reylanistan">Reylanistan</a></li>
            <li><a href="/nations/samborno">Samborno</a></li>
            <li><a href="/nations/surigan">Surigan</a></li>
            <li><a href="/nations/tiormulia">Tiormulia</a></li>
            <li><a href="/nations/ujarvia">Ujarvia</a></li>
          </ul>
        </li>
        <li>Cultures</li>
        <li>Organisations</li>
        <li>Peuples</li>
        <li>Créatures</li>
      </ul>
    </aside>
    <slot />

    <aside class="right-sider">Droite</aside>
  </main>

  <footer>
    <p>
      visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit
    </p>
  </footer>
</div>
