<!doctype html>
<!--
  index.html
  Page statique bilingue FR / EN prête à être déposée à la racine du dépôt GitHub

  Instructions :
  1) Remplace l'ancien fichier par celui-ci et nomme-le exactement `index.html` à la racine du repo.
  2) Dépose les images `Stars.png` et `ST-etienne-theatre.png` à la racine (même dossier que index.html).
  3) Active GitHub Pages (branche main, dossier: / root) si ce n'est pas déjà fait.
  4) Teste l'URL : https://danielleteil.github.io/danielle-teil-auteure/  (les boutons FR / EN basculent le texte)

  Remarque SEO : ce fichier utilise JSON-LD et meta tags. Pour une vraie stratégie SEO, créez aussi une page /en/index.html (optionnel) et soumettez l'URL à Google Search Console.
-->
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Teil Danielle — Écrivaine — "Quand les stars passent à table" • "Saint-Étienne et le théâtre"</title>
  <meta name="description" content="Page officielle de Teil Danielle — auteure, résumés et couvertures de ses ouvrages. Contact : dteil1243@gmail.com" />
  <meta name="keywords" content="Teil Danielle, écrivaine, auteur, théâtre, Saint-Étienne, biographie" />
  <meta property="og:title" content="Teil Danielle — Écrivaine" />
  <meta property="og:description" content="Auteure de 'Quand les stars passent à table' et 'Saint-Étienne et le théâtre'." />
  <meta property="og:type" content="profile" />
  <meta property="og:locale" content="fr_FR" />
  <link rel="alternate" hreflang="fr" href="/" />
  <link rel="alternate" hreflang="en" href="/?lang=en" />
  <style>
    :root{--bg:#fbfbfc;--card:#fff;--muted:#5b6170;--accent:#111827;--accent2:#6b7280}
    *{box-sizing:border-box}
    body{font-family:Georgia, 'Times New Roman', serif;margin:0;background:var(--bg);color:var(--accent);line-height:1.45}
    .wrap{max-width:960px;margin:36px auto;padding:24px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .title{font-size:28px;font-weight:700;letter-spacing:0.4px}
    .subtitle{color:var(--accent2);font-size:14px}
    .lang-toggle{display:flex;gap:8px}
    button.lang{border:1px solid #e6e9ef;background:transparent;padding:6px 10px;border-radius:8px;cursor:pointer}
    button.lang[aria-pressed="true"]{background:#111827;color:#fff}

    .cards{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:24px}
    .card{background:var(--card);padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(15,23,42,0.06)}
    .cover{width:100%;height:300px;border-radius:8px;overflow:hidden;display:flex;align-items:center;justify-content:center;background:#f3f4f6}
    .cover img{width:100%;height:100%;object-fit:cover}
    h3{margin:12px 0 6px 0;font-family:Georgia,serif}
    .meta{font-size:13px;color:var(--muted)}
    .desc{margin-top:10px;color:#222;font-size:15px}

    footer{margin-top:28px;padding-top:18px;border-top:1px solid #eef2ff;color:var(--muted);font-size:14px}

    /* Responsive */
    @media (max-width:720px){.cards{grid-template-columns:1fr}.cover{height:220px}.title{font-size:22px}}
  </style>
</head>
<body>
  <div class="wrap" role="main">
    <header>
      <div>
        <div class="title" id="name-display">Teil Danielle</div>
        <div class="subtitle" id="tagline">Écrivaine — Author</div>
      </div>
      <div>
        <div class="lang-toggle" role="tablist" aria-label="Language switch">
          <button class="lang" id="btn-fr" aria-pressed="true" aria-controls="content">FR</button>
          <button class="lang" id="btn-en" aria-pressed="false" aria-controls="content">EN</button>
        </div>
      </div>
    </header>

    <section class="cards" aria-label="Ouvrages" id="content">
      <article class="card" id="book1">
        <div class="cover"><img src="Stars.png" alt="Couverture — Quand les stars passent à table" id="cover1"/></div>
        <h3 class="title-book" id="title1">Quand les stars passent à table</h3>
        <div class="meta"><span class="pub-date" id="pub1">Septembre 1999</span> — <span class="publisher" id="pub1p">Indépendant</span></div>
        <div class="desc" id="desc1">Biographie d'un célèbre restaurateur, Marco Cruciani, qui recevait à sa table les stars du spectacle. Chacune d'entre elles lui laissaient une signature sur son livre d'or, qui comporte aujourd'hui plus de 3000 signatures. De Petrucciani à Jean-Jacques Goldman, de Jane Birkin à Pierre Bachelet, ils sont nombreux à s'être confiés à Marco.</div>
      </article>

      <article class="card" id="book2">
        <div class="cover"><img src="ST-etienne-theatre.png" alt="Couverture — Saint-Étienne et le théâtre" id="cover2"/></div>
        <h3 class="title-book" id="title2">Saint-Étienne et le théâtre</h3>
        <div class="meta"><span class="pub-date" id="pub2">Octobre 1990</span> — <span class="publisher" id="pub2p">Éditions Xavier Lejeune</span></div>
        <div class="desc" id="desc2">Du vaudeville à la comédie : 1650 - 1990. Trois siècles de vie locale, mais aussi une histoire qui dépasse largement les horizons de la ville et intègre l'histoire du théâtre en France. Saint-Étienne, le berceau de la décentralisation théâtrale, n'a sans doute jamais mieux mérité ce qualificatif avec l'histoire européenne qu'elle a amorcée. De grands hommes, comme Dasté, ont fait son histoire et aujourd'hui la Comédie de Saint-Étienne est un des plus grands centres dramatiques nationaux.</div>
      </article>
    </section>

    <footer>
      <div>Contact : <a href="mailto:dteil1243@gmail.com">dteil1243@gmail.com</a></div>
      
    </footer>
  </div>

  <script>
    // Translations for visible content and meta values
    const translations = {
      en: {
        tagline: 'Writer — Author',
        'title1': 'When the Stars Dine',
        'desc1': "Biography of the famous restaurateur Marco Cruciani, who hosted stars of the performing arts at his table. Each left a signature in his guestbook, which now holds over 3,000 signatures. From Petrucciani to Jean-Jacques Goldman, from Jane Birkin to Pierre Bachelet, many have confided in Marco.",
        'title2': 'Saint-Étienne and the Theatre',
        'desc2': "From vaudeville to comedy: 1650–1990. Three centuries of local life and an account that goes beyond the city to the history of theatre in France. Saint-Étienne, cradle of theatrical decentralisation, owes much to figures such as Dasté. Today the Comédie de Saint-Étienne is among the country's major dramatic centres.",
        'pub1_date': 'September 1999',
        'pub1_publisher': 'Independent',
        'pub2_date': 'October 1990',
        'pub2_publisher': 'Xavier Lejeune Editions',
        'alt1': 'Cover — When the Stars Dine',
        'alt2': 'Cover — Saint-Étienne and the Theatre'
      },
      fr: {
        tagline: 'Écrivaine — Author',
        'title1': "Quand les stars passent à table",
        'desc1': "Biographie d'un célèbre restaurateur, Marco Cruciani, qui recevait à sa table les stars du spectacle. Chacune d'entre elles lui laissaient une signature sur son livre d'or, qui comporte aujourd'hui plus de 3000 signatures. De Petrucciani à Jean-Jacques Goldman, de Jane Birkin à Pierre Bachelet, ils sont nombreux à s'être confiés à Marco.",
        'title2': 'Saint-Étienne et le théâtre',
        'desc2': "Du vaudeville à la comédie : 1650 - 1990. Trois siècles de vie locale, mais aussi une histoire qui dépasse largement les horizons de la ville et intègre l'histoire du théâtre en France. Saint-Étienne, le berceau de la décentralisation théâtrale, n'a sans doute jamais mieux mérité ce qualificatif avec l'histoire européenne qu'elle a amorcée. De grands hommes, comme Dasté, ont fait son histoire et aujourd'hui la Comédie de Saint-Étienne est un des plus grands centres dramatiques nationaux.",
        'pub1_date': 'Septembre 1999',
        'pub1_publisher': 'Indépendant',
        'pub2_date': 'Octobre 1990',
        'pub2_publisher': 'Éditions Xavier Lejeune',
        'alt1': 'Couverture — Quand les stars passent à table',
        'alt2': 'Couverture — Saint-Étienne et le théâtre'
      }
    };

    // Set language (updates visible text, alt attributes, and document lang)
    function setLang(lang){
      if(!translations[lang]) lang = 'fr';
      document.documentElement.lang = (lang === 'en') ? 'en' : 'fr';

      document.getElementById('tagline').textContent = translations[lang].tagline;
      document.getElementById('title1').textContent = translations[lang].title1;
      document.getElementById('desc1').textContent = translations[lang].desc1;
      document.getElementById('title2').textContent = translations[lang].title2;
      document.getElementById('desc2').textContent = translations[lang].desc2;

      document.getElementById('pub1').textContent = translations[lang].pub1_date;
      document.getElementById('pub1p').textContent = translations[lang].pub1_publisher;
      document.getElementById('pub2').textContent = translations[lang].pub2_date;
      document.getElementById('pub2p').textContent = translations[lang].pub2_publisher;

      document.getElementById('cover1').alt = translations[lang].alt1;
      document.getElementById('cover2').alt = translations[lang].alt2;

      // update ARIA pressed
      document.getElementById('btn-fr').setAttribute('aria-pressed', lang === 'fr' ? 'true' : 'false');
      document.getElementById('btn-en').setAttribute('aria-pressed', lang === 'en' ? 'true' : 'false');

      // Optionally update the URL query param without reloading
      try{ const u = new URL(window.location); u.searchParams.set('lang', lang); window.history.replaceState({}, '', u); }catch(e){}
    }

    // Buttons
    document.getElementById('btn-fr').addEventListener('click', ()=>setLang('fr'));
    document.getElementById('btn-en').addEventListener('click', ()=>setLang('en'));

    // Detect ?lang=en parameter or browser language on first load
    (function(){
      const q = new URLSearchParams(window.location.search).get('lang');
      if(q === 'en' || q === 'fr'){ setLang(q); return; }
      const nav = (navigator.languages && navigator.languages[0]) || navigator.language || 'fr';
      if(nav.startsWith('en')) setLang('en'); else setLang('fr');
    })();

    // JSON-LD for SEO
    (function(){
      const jsonld = {
        "@context":"https://schema.org",
        "@type":"Person",
        "name":"Teil Danielle",
        "email":"mailto:dteil1243@gmail.com",
        "knowsAbout":["théâtre","biographies","histoire locale"],
        "knowsLanguage":["fr","en"],
        "hasPublished":[
          {"@type":"CreativeWork","name":"Quand les stars passent à table","datePublished":"1999-09"},
          {"@type":"CreativeWork","name":"Saint-Étienne et le théâtre","datePublished":"1990-10","publisher":{"@type":"Organization","name":"Éditions Xavier Lejeune"}}
        ]
      };
      const s = document.createElement('script'); s.type='application/ld+json'; s.textContent = JSON.stringify(jsonld); document.head.appendChild(s);
    })();
  </script>
</body>
</html>
