<script>
  import { page } from "$app/stores";
  import "$lib/style/styles.css";
</script>

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
    <slot />
  </main>

  <footer>
    <p>
      visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit
    </p>
  </footer>
</div>
