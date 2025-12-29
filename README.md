<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>TOURISM A WAY OF LOVE — Delhi</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Discover Delhi by mood: fun, romantic, exotic, heritage gold, family fun, haunted, and religious. Scroll-play, themed sections, maps, prices, nearby gems." />
  <style>
    :root {
      --bg: #0f0f14;
      --text: #e6e6ea;
      --muted: #b5b5bd;
      --card: #1a1a21;
      --accent: #ff5a5f;
      --glow: rgba(255, 90, 95, 0.35);

      /* Category themes */
      --fun-bg: #10172a;
      --fun-text: #e2e8f0;
      --fun-accent: #22d3ee;
      --fun-card: #0b1220;
      --fun-glow: rgba(34, 211, 238, 0.35);

      --romantic-bg: #1a0f14;
      --romantic-text: #ffe6ea;
      --romantic-accent: #ff477e;
      --romantic-card: #230c16;
      --romantic-glow: rgba(255, 71, 126, 0.35);

      --exotic-bg: #0e1f1f;
      --exotic-text: #e0fff7;
      --exotic-accent: #06d6a0;
      --exotic-card: #072323;
      --exotic-glow: rgba(6, 214, 160, 0.35);

      --heritage-bg: #1b140a;
      --heritage-text: #f8edd9;
      --heritage-accent: #ffa62b;
      --heritage-card: #23180a;
      --heritage-glow: rgba(255, 166, 43, 0.35);

      --family-bg: #0f172a;
      --family-text: #e2e8f0;
      --family-accent: #60a5fa;
      --family-card: #0b1220;
      --family-glow: rgba(96, 165, 250, 0.35);

      --haunted-bg: #0a0a0a;
      --haunted-text: #d4d4d8;
      --haunted-accent: #7c3aed;
      --haunted-card: #111113;
      --haunted-glow: rgba(124, 58, 237, 0.35);

      --religious-bg: #0f1a12;
      --religious-text: #eaf4ea;
      --religious-accent: #7ebc59;
      --religious-card: #0a140c;
      --religious-glow: rgba(126, 188, 89, 0.35);
    }

    /* Base reset */
    * { box-sizing: border-box; }
    html, body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    /* Scroll delights */
    .parallax {
      position: fixed;
      inset: 0;
      z-index: -1;
      pointer-events: none;
      background:
        radial-gradient(1200px 500px at 10% 10%, var(--glow), transparent 60%),
        radial-gradient(900px 400px at 90% 40%, var(--glow), transparent 55%),
        linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.2));
      filter: blur(40px) saturate(1.05);
      opacity: 0.7;
      transition: 300ms ease;
    }
    .grain::before {
      content: "";
      position: fixed;
      inset: 0;
      z-index: -1;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.6' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.045'/%3E%3C/svg%3E");
      background-size: 160px 160px;
      mix-blend-mode: overlay;
      pointer-events: none;
    }

    /* Header */
    header {
      position: sticky;
      top: 0;
      backdrop-filter: blur(10px);
      background: linear-gradient(0deg, rgba(0,0,0,0.15), rgba(0,0,0,0.25));
      border-bottom: 1px solid rgba(255,255,255,0.08);
      z-index: 100;
    }
    .nav {
      display: flex;
      align-items: center;
      gap: 16px;
      padding: 14px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }
    .brand {
      font-weight: 700;
      letter-spacing: 0.4px;
      color: var(--accent);
      text-transform: uppercase;
      font-size: 14px;
      white-space: nowrap;
    }
    .tabs {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }
    .tab {
      border: 1px solid rgba(255,255,255,0.12);
      background: rgba(255,255,255,0.03);
      color: var(--text);
      padding: 8px 12px;
      border-radius: 12px;
      cursor: pointer;
      font-size: 13px;
      transition: 180ms ease;
    }
    .tab:hover { transform: translateY(-1px); border-color: rgba(255,255,255,0.2); }
    .tab.active { background: var(--accent); color: #0b0b0b; border-color: transparent; }

    .actions {
      margin-left: auto;
      display: flex;
      gap: 8px;
    }
    .btn {
      background: rgba(255,255,255,0.08);
      color: var(--text);
      border: 1px solid rgba(255,255,255,0.12);
      padding: 8px 12px;
      border-radius: 10px;
      font-size: 13px;
      cursor: pointer;
      transition: 180ms ease;
    }
    .btn:hover { background: rgba(255,255,255,0.14); }

    /* Hero */
    .hero {
      display: grid;
      place-items: center;
      text-align: center;
      padding: 64px 20px 24px;
    }
    .hero h1 {
      font-size: clamp(28px, 4vw, 44px);
      line-height: 1.05;
      margin: 0 0 12px;
      letter-spacing: 0.3px;
    }
    .hero p {
      margin: 0 auto;
      max-width: 820px;
      color: var(--muted);
      font-size: 15px;
    }

    /* Theme banner */
    .theme-banner {
      margin: 22px auto;
      padding: 12px 16px;
      max-width: 860px;
      border-radius: 12px;
      border: 1px dashed rgba(255,255,255,0.16);
      background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(0,0,0,0.12));
      color: var(--muted);
      font-size: 13px;
    }

    /* Sections */
    section {
      padding: 26px 20px 10px;
    }
    .section-title {
      max-width: 1200px;
      margin: 0 auto 10px;
      display: flex;
      align-items: baseline;
      gap: 12px;
    }
    .section-title h2 {
      margin: 0;
      font-size: 20px;
      letter-spacing: 0.2px;
    }
    .section-title .hint {
      color: var(--muted);
      font-size: 13px;
    }

    /* Grid */
    .grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 16px;
      max-width: 1200px;
      margin: 0 auto 10px;
    }
    .card {
      grid-column: span 6;
      background: var(--card);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 16px;
      overflow: clip;
      position: relative;
      transition: transform 200ms ease, box-shadow 200ms ease, border-color 200ms ease;
    }
    @media (max-width: 920px) { .card { grid-column: span 12; } }
    .card:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 30px rgba(0,0,0,0.30), 0 0 0 10px var(--glow);
      border-color: rgba(255,255,255,0.16);
    }
    .card-header {
      padding: 14px 16px 12px;
      border-bottom: 1px solid rgba(255,255,255,0.08);
      display: flex; align-items: center; gap: 10px;
      background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(0,0,0,0.12));
    }
    .badge {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 20px;
      background: var(--accent);
      color: #0b0b0b;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
    }
    .card h3 { margin: 0; font-size: 18px; }
    .card-body { padding: 12px 16px 14px; display: grid; gap: 8px; }
    .meta { display: flex; flex-wrap: wrap; gap: 10px; color: var(--muted); font-size: 13px; }
    .meta span { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); padding: 6px 10px; border-radius: 12px; }
    .desc { color: var(--text); font-size: 14px; }
    .links { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px; }
    .link {
      padding: 8px 10px;
      border-radius: 10px;
      border: 1px solid rgba(255,255,255,0.14);
      background: rgba(255,255,255,0.05);
      color: var(--text);
      font-size: 13px;
      text-decoration: none;
      transition: 160ms ease;
    }
    .link:hover { background: var(--accent); color: #0b0b0b; border-color: transparent; }

    /* Category sections with mood themes */
    .category.fun     { --bg: var(--fun-bg); --text: var(--fun-text); --accent: var(--fun-accent); --card: var(--fun-card); --glow: var(--fun-glow); }
    .category.romantic{ --bg: var(--romantic-bg); --text: var(--romantic-text); --accent: var(--romantic-accent); --card: var(--romantic-card); --glow: var(--romantic-glow); }
    .category.exotic  { --bg: var(--exotic-bg); --text: var(--exotic-text); --accent: var(--exotic-accent); --card: var(--exotic-card); --glow: var(--exotic-glow); }
    .category.heritage{ --bg: var(--heritage-bg); --text: var(--heritage-text); --accent: var(--heritage-accent); --card: var(--heritage-card); --glow: var(--heritage-glow); }
    .category.family  { --bg: var(--family-bg); --text: var(--family-text); --accent: var(--family-accent); --card: var(--family-card); --glow: var(--family-glow); }
    .category.haunted { --bg: var(--haunted-bg); --text: var(--haunted-text); --accent: var(--haunted-accent); --card: var(--haunted-card); --glow: var(--haunted-glow); }
    .category.religious{--bg: var(--religious-bg); --text: var(--religious-text); --accent: var(--religious-accent); --card: var(--religious-card); --glow: var(--religious-glow); }

    /* Mood header art */
    .mood {
      position: relative;
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.10);
      border-radius: 16px;
      margin: 16px auto;
      max-width: 1200px;
      background: linear-gradient(90deg, rgba(255,255,255,0.03), rgba(0,0,0,0.15));
    }
    .mood .canvas {
      height: 120px;
      background:
        radial-gradient(220px 60px at 20% 80%, var(--glow), transparent 60%),
        radial-gradient(160px 50px at 80% 20%, var(--glow), transparent 55%),
        linear-gradient(180deg, rgba(255,255,255,0.03), rgba(0,0,0,0.2));
      filter: saturate(1.15);
    }
    .mood .copy { position: absolute; inset: 0; display: grid; place-items: center; text-align: center; padding: 12px; }
    .mood h3 { margin: 0; font-size: 16px; letter-spacing: 0.2px; }
    .mood p { margin: 6px 0 0; font-size: 13px; color: var(--muted); }

    /* Footer with upload */
    footer {
      margin-top: 30px;
      padding: 22px 20px 36px;
      border-top: 1px solid rgba(255,255,255,0.08);
      background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(0,0,0,0.12));
    }
    .footer-inner {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      gap: 14px;
      align-items: center;
      grid-template-columns: 100px 1fr;
    }
    .avatar {
      width: 90px; height: 90px; border-radius: 50%;
      border: 2px solid var(--accent);
      object-fit: cover; background: rgba(255,255,255,0.05);
    }
    .footer-inner h4 { margin: 0; font-size: 16px; }
    .upload {
      display: flex; gap: 8px; align-items: center; margin-top: 6px;
    }
    .credit { color: var(--muted); font-size: 12px; }

    /* Scroll cue */
    .scroll-cue {
      position: fixed; bottom: 16px; right: 16px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.10);
      padding: 8px 10px; border-radius: 10px;
      font-size: 12px; color: var(--muted);
    }
  </style>
</head>
<body class="grain">

  <div class="parallax" id="parallax"></div>

  <header>
    <nav class="nav">
      <div class="brand">TOURISM A WAY OF LOVE — Delhi</div>
      <div class="tabs" id="tabs">
        <button class="tab active" data-target="fun">Fun places</button>
        <button class="tab" data-target="romantic">Romantic places</button>
        <button class="tab" data-target="exotic">Exotic places</button>
        <button class="tab" data-target="heritage">Heritage gold</button>
        <button class="tab" data-target="family">Family fun</button>
        <button class="tab" data-target="haunted">Haunted places</button>
        <button class="tab" data-target="religious">Religious places</button>
      </div>
      <div class="actions">
        <button class="btn" id="shuffle">Shuffle ideas</button>
        <button class="btn" id="theme">Surprise theme</button>
      </div>
    </nav>
  </header>

  <div class="hero">
    <h1>Find your Delhi, by mood.</h1>
    <p>Scroll through themed vibes and curated spots. Tap a card for maps, prices, and nearby gems. Let the city meet your curiosity.</p>
    <div class="theme-banner" id="themeBanner">Current mood: Fun — neon nights, street bites, playful parks.</div>
  </div>

  <!-- Fun places -->
  <section id="fun" class="category fun">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Playful energy</h3>
        <p>Color-pop UI, lively hover states, and night glow accents.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Fun places</h2>
      <span class="hint">Street food, quirky parks, and bustle.</span>
    </div>
    <div class="grid" id="grid-fun"></div>
  </section>

  <!-- Romantic places -->
  <section id="romantic" class="category romantic">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Warm & intimate</h3>
        <p>Soft gradients, rose highlights, and calm motion.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Romantic places</h2>
      <span class="hint">Sunsets, gardens, quiet corners.</span>
    </div>
    <div class="grid" id="grid-romantic"></div>
  </section>

  <!-- Exotic places -->
  <section id="exotic" class="category exotic">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Chic & fresh</h3>
        <p>Tropical hues, luxe vibes, and crisp lines.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Exotic places</h2>
      <span class="hint">Stylish scenes and standout experiences.</span>
    </div>
    <div class="grid" id="grid-exotic"></div>
  </section>

  <!-- Heritage gold -->
  <section id="heritage" class="category heritage">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Timeless textures</h3>
        <p>Amber glow, serif accents, and subtle grain.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Heritage gold</h2>
      <span class="hint">UNESCO sites, forts, tombs.</span>
    </div>
    <div class="grid" id="grid-heritage"></div>
  </section>

  <!-- Family fun -->
  <section id="family" class="category family">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Bright & friendly</h3>
        <p>Accessible contrast, playful edges, and clear info.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Family fun</h2>
      <span class="hint">Museums, zoos, hands-on learning.</span>
    </div>
    <div class="grid" id="grid-family"></div>
  </section>

  <!-- Haunted places -->
  <section id="haunted" class="category haunted">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Shadow & shimmer</h3>
        <p>Deep blacks, eerie purples, and soft fog.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Haunted places</h2>
      <span class="hint">Local lore, legends, and whispers.</span>
    </div>
    <div class="grid" id="grid-haunted"></div>
  </section>

  <!-- Religious places (10+) -->
  <section id="religious" class="category religious">
    <div class="mood">
      <div class="canvas"></div>
      <div class="copy">
        <h3>Peace & symmetry</h3>
        <p>Gentle greens, mindful spacing, and calm rhythm.</p>
      </div>
    </div>
    <div class="section-title">
      <h2>Religious places</h2>
      <span class="hint">Temples, mosques, gurdwaras, and more.</span>
    </div>
    <div class="grid" id="grid-religious"></div>
  </section>

  <footer>
    <div class="footer-inner">
      <img id="ishaan-photo" class="avatar" alt="Ishaan Mehndiratta" />
      <div>
        <h4>ISHAAN MEHNDIRATTA</h4>
        <p class="credit">Add your photo below — it will appear here instantly and be saved locally in your browser.</p>
        <div class="upload">
          <input type="file" id="photoInput" accept="image/*" />
          <button class="btn" id="savePhoto">Save photo</button>
        </div>
      </div>
    </div>
  </footer>

  <div class="scroll-cue">Tip: Use the tabs to jump themes. Hover cards for glow.</div>

  <script>
    // Data: name, area, price, maps, desc, nearby
    const data = {
      fun: [
        { name: "Dilli Haat (INA)", area: "INA, South Delhi", price: "Ticketed", maps: "https://www.google.com/maps?q=Dilli+Haat+INA+Delhi", desc: "Crafts, music, and pan-India street food under one vibrant bazaar.", nearby: ["Lodhi Garden", "Safdarjung Tomb"] },
        { name: "Waste to Wonder Park", area: "Sarai Kale Khan", price: "Ticketed", maps: "https://www.google.com/maps?q=Waste+to+Wonder+Park+Delhi", desc: "Seven world wonders recreated from scrap—quirky photo ops galore.", nearby: ["Humayun's Tomb", "Nizamuddin Basti"] },
        { name: "Adventure Island", area: "Rohini", price: "Ticketed", maps: "https://www.google.com/maps?q=Adventure+Island+Rohini", desc: "Roller coasters, rides, and lakeside walkways for all ages.", nearby: ["Japanese Park", "Metro Walk Mall"] },
        { name: "India Gate lawns", area: "Central Delhi", price: "Free", maps: "https://www.google.com/maps?q=India+Gate+New+Delhi", desc: "Evening strolls, ice cream, and lit-up monument views.", nearby: ["Kartavya Path", "National War Memorial"] },
        { name: "Hudson Lane cafés", area: "GTB Nagar", price: "Varies", maps: "https://www.google.com/maps?q=Hudson+Lane+Delhi", desc: "Student hub with Instagrammable cafés and pocket-friendly bites.", nearby: ["Majnu ka Tila", "Bonta Park"] },
      ],
      romantic: [
        { name: "Lodhi Garden", area: "Lodhi Estate", price: "Free", maps: "https://www.google.com/maps?q=Lodhi+Garden+Delhi", desc: "Serene lawns, ancient tombs, and golden-hour benches.", nearby: ["Khan Market", "Safdarjung Tomb"] },
        { name: "Garden of Five Senses", area: "Saket", price: "Ticketed", maps: "https://www.google.com/maps?q=Garden+of+Five+Senses+Delhi", desc: "Art installations, fragrant pathways, and secluded nooks.", nearby: ["Qutub Minar", "Champa Gali"] },
        { name: "Hauz Khas Fort & Lake", area: "Hauz Khas", price: "Ticketed (fort)", maps: "https://www.google.com/maps?q=Hauz+Khas+Fort+Delhi", desc: "Ruins meeting a tranquil lake, with cafés steps away.", nearby: ["Deer Park", "Green Park Market"] },
        { name: "Sunder Nursery", area: "Nizamuddin", price: "Ticketed", maps: "https://www.google.com/maps?q=Sunder+Nursery+Delhi", desc: "Heritage park with mosaics, lakes, and flowering alleys.", nearby: ["Humayun's Tomb", "Nizamuddin Dargah"] },
        { name: "Qutub Minar vistas", area: "Mehrauli", price: "Ticketed", maps: "https://www.google.com/maps?q=Qutub+Minar+Delhi", desc: "Majestic stonework and sunset silhouettes.", nearby: ["Mehrauli Archeological Park", "Chhatarpur Temple"] },
      ],
      exotic: [
        { name: "Aerocity promenade", area: "Aerocity", price: "Varies", maps: "https://www.google.com/maps?q=Aerocity+Delhi", desc: "Designer hotels, global dining, and lit boulevard nights.", nearby: ["DLF Promenade", "Vasant Kunj"] },
        { name: "Khan Market", area: "Near India Gate", price: "Varies", maps: "https://www.google.com/maps?q=Khan+Market+Delhi", desc: "Boutique shopping and stylish eateries.", nearby: ["Lodhi Garden", "India Habitat Centre"] },
        { name: "Champa Gali", area: "Saket", price: "Varies", maps: "https://www.google.com/maps?q=Champa+Gali+Delhi", desc: "Fairy-light lanes, indie cafés, craft studios.", nearby: ["Garden of Five Senses", "Select Citywalk"] },
        { name: "The Lodhi waterfront", area: "Lodhi Road", price: "Varies", maps: "https://www.google.com/maps?q=The+Lodhi+Hotel+Delhi", desc: "Quiet luxury with tree-lined walks.", nearby: ["Lodhi Garden", "India Habitat Centre"] },
        { name: "Mehrauli Archaeological Park", area: "Mehrauli", price: "Free", maps: "https://www.google.com/maps?q=Mehrauli+Archaeological+Park+Delhi", desc: "Scattered ruins, stepwells, and photo-rich trails.", nearby: ["Qutub Minar", "Garden of Five Senses"] },
      ],
      heritage: [
        { name: "Red Fort (Lal Qila)", area: "Old Delhi", price: "Ticketed", maps: "https://www.google.com/maps?q=Red+Fort+Delhi", desc: "UNESCO fortress with Mughal grandeur and museums.", nearby: ["Chandni Chowk", "Jama Masjid"] },
        { name: "Humayun’s Tomb", area: "Nizamuddin", price: "Ticketed", maps: "https://www.google.com/maps?q=Humayun's+Tomb+Delhi", desc: "Persian gardens and perfect symmetry—UNESCO-listed.", nearby: ["Sunder Nursery", "Hazrat Nizamuddin"] },
        { name: "Qutub Minar", area: "Mehrauli", price: "Ticketed", maps: "https://www.google.com/maps?q=Qutub+Minar+Delhi", desc: "Soaring victory tower in the Qutub complex.", nearby: ["Mehrauli Archaeological Park", "Chhatarpur"] },
        { name: "Purana Qila (Old Fort)", area: "Pragati Maidan", price: "Ticketed", maps: "https://www.google.com/maps?q=Purana+Qila+Delhi", desc: "Ancient ramparts, boat lake, and museum.", nearby: ["National Zoological Park", "Humayun’s Tomb"] },
        { name: "Safdarjung Tomb", area: "Lodi Road", price: "Ticketed", maps: "https://www.google.com/maps?q=Safdarjung+Tomb+Delhi", desc: "Late-Mughal mausoleum with palm-lined vistas.", nearby: ["Lodhi Garden", "Jor Bagh"] },
      ],
      family: [
        { name: "National Rail Museum", area: "Chanakyapuri", price: "Ticketed", maps: "https://www.google.com/maps?q=National+Rail+Museum+Delhi", desc: "Vintage engines, toy train rides, and interactive exhibits.", nearby: ["Nehru Park", "Delhi Haat (INA)"] },
        { name: "National Zoological Park", area: "Mathura Road", price: "Ticketed", maps: "https://www.google.com/maps?q=National+Zoological+Park+Delhi", desc: "Expansive zoo with shaded trails and diverse species.", nearby: ["Purana Qila", "Humayun’s Tomb"] },
        { name: "Nehru Planetarium", area: "Teen Murti", price: "Ticketed", maps: "https://www.google.com/maps?q=Nehru+Planetarium+Delhi", desc: "Sky theatre shows and space exhibits for kids.", nearby: ["Nehru Memorial Museum", "Chanakyapuri"] },
        { name: "Children’s Park (India Gate)", area: "Central Delhi", price: "Free", maps: "https://www.google.com/maps?q=Children's+Park+India+Gate+Delhi", desc: "Play zones, mini train, and open lawns.", nearby: ["India Gate", "Kartavya Path"] },
        { name: "National Science Centre", area: "Pragati Maidan", price: "Ticketed", maps: "https://www.google.com/maps?q=National+Science+Centre+Delhi", desc: "Hands-on science galleries and fun demos.", nearby: ["Pragati Maidan", "Purana Qila"] },
      ],
      haunted: [
        { name: "Agrasen ki Baoli", area: "KG Marg", price: "Free", maps: "https://www.google.com/maps?q=Agrasen+ki+Baoli+Delhi", desc: "Ancient stepwell with stories of echoes and emptiness.", nearby: ["Connaught Place", "Jantar Mantar"] },
        { name: "Khooni Darwaza", area: "Near Delhi Gate", price: "Free", maps: "https://www.google.com/maps?q=Khooni+Darwaza+Delhi", desc: "Historic gateway tied to darker chapters.", nearby: ["Feroz Shah Kotla", "Daryaganj"] },
        { name: "Jamali Kamali", area: "Mehrauli", price: "Free", maps: "https://www.google.com/maps?q=Jamali+Kamali+Delhi", desc: "Mosque-tomb complex with whispered legends.", nearby: ["Qutub Minar", "Mehrauli Park"] },
        { name: "Sanjay Van", area: "Qutub Institutional Area", price: "Free", maps: "https://www.google.com/maps?q=Sanjay+Van+Delhi", desc: "Dense forest trails and twilight tales.", nearby: ["Qutub Minar", "Hauz Khas"] },
        { name: "Feroz Shah Kotla", area: "Bahadur Shah Zafar Marg", price: "Ticketed", maps: "https://www.google.com/maps?q=Feroz+Shah+Kotla+Fort+Delhi", desc: "Medieval ruins and local djinn lore.", nearby: ["Khooni Darwaza", "Pragati Maidan"] },
        { name: "Bhuli Bhatiyari ka Mahal", area: "Jhandewalan Ridge", price: "Free", maps: "https://www.google.com/maps?q=Bhuli+Bhatiyari+ka+Mahal+Delhi", desc: "Ridge ruins with an eerie quiet.", nearby: ["Karol Bagh", "Rajendra Place"] },
        { name: "Malcha Mahal", area: "Chanakyapuri Ridge", price: "Restricted/Exterior", maps: "https://www.google.com/maps?q=Malcha+Mahal+Delhi", desc: "Royal ruin hidden in the forest.", nearby: ["Nehru Park", "Chanakyapuri"] },
        { name: "Lothian Cemetery", area: "Old Delhi", price: "Free", maps: "https://www.google.com/maps?q=Lothian+Cemetery+Delhi", desc: "Colonial-era graves and age-old tales.", nearby: ["Red Fort", "Chandni Chowk"] },
        { name: "Delhi Cantonment (certain stretches)", area: "Delhi Cantt", price: "Free", maps: "https://www.google.com/maps?q=Delhi+Cantonment", desc: "Late-night drives with rumored sightings.", nearby: ["Dhaula Kuan", "Army Golf Course"] },
        { name: "Dwarka Sector 9 periphery", area: "Dwarka", price: "Free", maps: "https://www.google.com/maps?q=Dwarka+Sector+9+Delhi", desc: "Urban legends along quieter roads.", nearby: ["Pacific D21 Mall", "Sector markets"] },
      ],
      religious: [
        { name: "Akshardham Temple", area: "NH-24", price: "Free (complex), Ticketed (exhibitions)", maps: "https://www.google.com/maps?q=Akshardham+Temple+Delhi", desc: "Grand temple complex with intricate carvings and cultural exhibits.", nearby: ["Commonwealth Games Village", "Yamuna Riverfront"] },
        { name: "Lotus Temple (Bahá’í House)", area: "Kalkaji", price: "Free", maps: "https://www.google.com/maps?q=Lotus+Temple+Delhi", desc: "Iconic lotus-shaped temple for silent prayer.", nearby: ["Kalkaji Mandir", "Nehru Place"] },
        { name: "Gurudwara Bangla Sahib", area: "Connaught Place", price: "Free", maps: "https://www.google.com/maps?q=Gurudwara+Bangla+Sahib+Delhi", desc: "Serene Sikh gurdwara with sarovar and langar.", nearby: ["CP Inner Circle", "Janpath"] },
        { name: "Jama Masjid", area: "Old Delhi", price: "Free (camera charges may apply)", maps: "https://www.google.com/maps?q=Jama+Masjid+Delhi", desc: "One of India’s largest mosques with city views.", nearby: ["Chandni Chowk", "Red Fort"] },
        { name: "ISKCON Temple (East of Kailash)", area: "East of Kailash", price: "Free", maps: "https://www.google.com/maps?q=ISKCON+Temple+Delhi", desc: "Vaishnav temple known for kirtans and exhibits.", nearby: ["Kailash Colony", "Nehru Place"] },
        { name: "Chhatarpur Temple", area: "Chhatarpur", price: "Free", maps: "https://www.google.com/maps?q=Chhatarpur+Temple+Delhi", desc: "Expansive complex devoted to Goddess Katyayani.", nearby: ["Qutub Minar", "Saket"] },
        { name: "Kalkaji Mandir", area: "Kalkaji", price: "Free", maps: "https://www.google.com/maps?q=Kalkaji+Mandir+Delhi", desc: "Ancient temple dedicated to the goddess Kali.", nearby: ["Lotus Temple", "Nehru Place"] },
        { name: "Gauri Shankar Temple", area: "Chandni Chowk", price: "Free", maps: "https://www.google.com/maps?q=Gauri+Shankar+Temple+Delhi", desc: "Historic Shiva temple with revered lingam.", nearby: ["Digambar Jain Lal Mandir", "Red Fort"] },
        { name: "Hanuman Mandir (CP)", area: "Connaught Place", price: "Free", maps: "https://www.google.com/maps?q=Hanuman+Mandir+Connaught+Place+Delhi", desc: "Popular temple known for Tuesday crowds.", nearby: ["Bangla Sahib", "Jantar Mantar"] },
        { name: "Shri Digambar Jain Lal Mandir", area: "Chandni Chowk", price: "Free", maps: "https://www.google.com/maps?q=Digambar+Jain+Lal+Mandir+Delhi", desc: "Oldest Jain temple in Delhi opposite Red Fort.", nearby: ["Red Fort", "Chandni Chowk"] },
      ]
    };

    // Render cards
    function renderCategory(id, items) {
      const grid = document.getElementById(`grid-${id}`);
      grid.innerHTML = "";
      items.forEach(item => {
        const el = document.createElement("article");
        el.className = "card";
        el.innerHTML = `
          <div class="card-header">
            <span class="badge">${id.toUpperCase()}</span>
            <h3>${item.name}</h3>
          </div>
          <div class="card-body">
            <div class="meta">
              <span><strong>Area:</strong> ${item.area}</span>
              <span><strong>Price:</strong> ${item.price}</span>
            </div>
            <p class="desc">${item.desc}</p>
            <div class="links">
              <a class="link" href="${item.maps}" target="_blank" rel="noopener">Open in Google Maps</a>
              ${item.nearby?.length ? `<span class="link" style="cursor:default"><strong>Nearby:</strong> ${item.nearby.join(", ")}</span>` : ""}
            </div>
          </div>
        `;
        grid.appendChild(el);
      });
    }
    renderCategory("fun", data.fun);
    renderCategory("romantic", data.romantic);
    renderCategory("exotic", data.exotic);
    renderCategory("heritage", data.heritage);
    renderCategory("family", data.family);
    renderCategory("haunted", data.haunted);
    renderCategory("religious", data.religious);

    // Tabs and theme switching
    const tabs = document.querySelectorAll(".tab");
    const banner = document.getElementById("themeBanner");
    const moods = {
      fun: "Fun — neon nights, street bites, playful parks.",
      romantic: "Romantic — warm tones, quiet corners, sunset paths.",
      exotic: "Exotic — chic streets, luxe stops, fresh palettes.",
      heritage: "Heritage — amber grains, monuments, timeless arches.",
      family: "Family — bright contrast, hands-on museums, safe fun.",
      haunted: "Haunted — shadow plays, whispered legends, ridge walks.",
      religious: "Religious — peaceful greens, mindful spaces, serene domes."
    };
    tabs.forEach(t => {
      t.addEventListener("click", () => {
        tabs.forEach(x => x.classList.remove("active"));
        t.classList.add("active");
        const target = t.dataset.target;
        document.getElementById(target).scrollIntoView({ behavior: "smooth", block: "start" });
        banner.textContent = `Current mood: ${moods[target]}`;
        applyParallaxTheme(target);
      });
    });

    // Parallax mood tint
    function applyParallaxTheme(cat) {
      const el = document.getElementById("parallax");
      const map = {
        fun:   ["var(--fun-glow)", "var(--fun-accent)"],
        romantic: ["var(--romantic-glow)", "var(--romantic-accent)"],
        exotic: ["var(--exotic-glow)", "var(--exotic-accent)"],
        heritage: ["var(--heritage-glow)", "var(--heritage-accent)"],
        family: ["var(--family-glow)", "var(--family-accent)"],
        haunted: ["var(--haunted-glow)", "var(--haunted-accent)"],
        religious: ["var(--religious-glow)", "var(--religious-accent)"]
      }[cat];
      el.style.opacity = 0.8;
      el.style.background =
        `radial-gradient(1200px 500px at 10% 10%, ${map[0]}, transparent 60%),`+
        `radial-gradient(900px 400px at 90% 40%, ${map[0]}, transparent 55%),`+
        `linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.2))`;
    }

    // Scroll-aware tint changes
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          applyParallaxTheme(e.target.id);
          banner.textContent = `Current mood: ${moods[e.target.id]}`;
          tabs.forEach(x => x.classList.toggle("active", x.dataset.target === e.target.id));
        }
      });
    }, { rootMargin: "-30% 0px -60% 0px", threshold: 0.01 });
    ["fun","romantic","exotic","heritage","family","haunted","religious"].forEach(id => observer.observe(document.getElementById(id)));

    // Shuffle to spark ideas
    document.getElementById("shuffle").addEventListener("click", () => {
      const id = document.querySelector(".tab.active").dataset.target;
      const arr = [...data[id]];
      for (let i = arr.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [arr[i], arr[j]] = [arr[j], arr[i]];
      }
      renderCategory(id, arr);
    });

    // Surprise theme
    document.getElementById("theme").addEventListener("click", () => {
      const cats = ["fun","romantic","exotic","heritage","family","haunted","religious"];
      const pick = cats[Math.floor(Math.random() * cats.length)];
      document.querySelector(`[data-target="${pick}"]`).click();
    });

    // Ishaan photo upload & persist
    const photoEl = document.getElementById("ishaan-photo");
    const inputEl = document.getElementById("photoInput");
    const saveBtn = document.getElementById("savePhoto");

    // Load saved photo
    const saved = localStorage.getItem("ishaan-photo");
    if (saved) photoEl.src = saved;

    inputEl.addEventListener("change", (e) => {
      const file = e.target.files?.[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = (ev) => { photoEl.src = ev.target.result; };
      reader.readAsDataURL(file);
    });
    saveBtn.addEventListener("click", () => {
      if (!photoEl.src) return alert("Please select a photo first.");
      localStorage.setItem("ishaan-photo", photoEl.src);
      alert("Photo saved to your browser.");
    });
  </script>
</body>
</html>
