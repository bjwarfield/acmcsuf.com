<script lang="ts">
  import Navbar from "@/components/sections/navbar.svelte";
  import Footer from "@/components/sections/footer.svelte";
  import SkipNavbarContent from "@/components/utils/skip-navbar-content.svelte";
  export let segment: string;
  const pageTitle = segment === undefined ? "ACM at CSUF" : segment;
</script>

<Navbar segment="{segment}" />
<SkipNavbarContent />
<main><slot /></main>
<Footer />

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>{`acmCSUF | ${pageTitle}`}</title>
  <link
    rel="apple-touch-icon"
    sizes="180x180"
    href="/assets/favicon/apple-touch-icon.png"
  />
  <link
    rel="icon"
    type="image/png"
    sizes="32x32"
    href="/assets/favicon/favicon-32x32.png"
  />
  <link
    rel="icon"
    type="image/png"
    sizes="16x16"
    href="/assets/favicon/favicon-16x16.png"
  />
  <link rel="manifest" href="/assets/favicon/site.webmanifest" />
  <link
    rel="mask-icon"
    href="/assets/favicon/safari-pinned-tab.svg"
    color="#000000"
  />
  <link rel="shortcut icon" href="/assets/favicon/favicon.ico" />
  <meta name="msapplication-TileColor" content="#000000" />
  <meta
    name="msapplication-config"
    content="/assets/favicon/browserconfig.xml"
  />
  <meta name="theme-color" content="#000" />
  <link rel="alternate" type="application/rss+xml" href="/feed.xml" />
</svelte:head>
