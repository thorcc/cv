<script>
  let hidden = true;
  const hiddenstring = {
    text1: "thorchrcow",
    text2: "gmail.com",
  };
</script>

<main>

  <div id="info">
    <h1>Thor Christian Coward</h1>
    <p>Lektor, sivilingeniør og utvikler</p>
  </div>

  <img src="/bilde.jpg" alt="Thor Christian står på huk ved siden av en tøff bil"/>
  
  <div>
    <h2>Arbeid</h2>
    <ul>
      <li>Lærer på Sandvika Videregående Skole, underviser i matematikk, IT1 og IT2</li>
    </ul>

    <h2>Utdanning</h2>
    <ul>
      <li>UiO: Faglig påfyll - 60 studiepoeng i informatikk</li>
      <li>UiO: Praktisk pedagogisk utdanning (PPU)</li>
      <li>NTNU: Produktutvikling og produksjon (2-årig master)</li>
      <li>HiOA: Maskiningeniør (bachelor)</li>
    </ul>

    <h2>Prosjekter</h2>
    <ul>
      <li><a target="_blank" href="https://jonasropstad.netlify.app/">jonasropstad.netlify.app</a> - portefølje for billedkunstneren Jonas Ropstad</li>
      <li><a href="https://bits-og-bytes.netlify.app/">bits-og-bytes.netlify.app</a> - visualisering av totallsystemet</li>
      <li><a target="_blank" href="https://setify.netlify.app">setify.netlify.app</a> - webapp som lager Spotify-spillelister fra setlister</li>
      <li><a target="_blank" href="https://artist-img.glitch.me/">artist-img.glitch.me</a> - søkemotor for artistbilder</li>
      <li><a target="_blank" href="https://www.wagland.art/">wagland.art</a> - portefølje for billedkunstneren Roger Wagland</li>
      <li><a target="_blank" href="https://sandvika.it">sandvika.it</a> - digital lærebok for IT1</li>
    </ul>

    <h2>IT-kompetanse</h2>

    <h3>Teknologier</h3>
    <ul>
      <li>Webutvikling - HTML, CSS, Javascript, Node, ReactJS, NextJS, Gatsby, Svelte, SvelteKit ++</li>
      <li>Databaser og CMS - SQL, Firebase, Sanity, Contentful</li>
      <li>Ingeniørarbeid - KBE (AML), 3D-modellering, algoritmer og datastrukturer</li>
      <li>Multimedier - Photoshop, Illustrator, XD, Premiere Pro, Audition</li>
    </ul>
    <h3>Programmeringsspråk</h3>
    <ul>
      <li>Javascript</li>
      <li>Typescript</li>
      <li>Python</li>
      <li>Java</li>
      <li>Lisp (<a target="_blank" href="https://www.technosoft.com/application-software/adaptive-modeling-language/">AML</a>)</li>
    </ul>

    <h2>Diverse</h2>
    <ul>
      <li><a href="https://github.com/thorcc" target="_blank">github.com/thorcc</a></li>
      <li id="mail" on:click={() => (hidden = !hidden)}>
        {#if hidden}
          klikk her for å vise epost
        {:else}
          {hiddenstring.text1}@{hiddenstring.text2}
        {/if}
      </li>
    </ul>
  </div>

</main>

<style>
  main {
    font-family: "Roboto", sans-serif;
    padding: 8px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 1200px;
    margin: auto;
    max-width: 95%;
    column-gap: 20px;
  }
  img {
    grid-row: span 2;
    width: 100%;
    min-height: 98vh;
    object-fit: cover;
  }
  h2 {
    text-decoration: underline;
  }
  a {
    color: black;
  }
  #mail {
    cursor: pointer;
    border-bottom: solid 1px black;
    width: fit-content;
    padding: 1px;
  }
  #mail:hover::marker {
    color: black;
  }
  #mail:hover {
    color: white;
    background-color: black;
  }
  @media only screen and (max-width: 1000px) {
    main {
      grid-template-columns: 1fr;
    }
    img {
      grid-row: span 1;
      min-height: auto;
      max-height: 500px;
      object-fit: cover;
      display: block;
    }
  }
  @media only screen and (max-width: 900px) and (max-height: 670px) {
    img {
      max-height: 300px;
    }
  }
</style>
