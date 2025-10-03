<!doctype html>
<html lang="en">
<head>
  <!-- =========================
       Core OS — Book Landing / Storefront
       Single-file static site, no build step required.
       Author brand: Henrik Forrest (Tanner Peterson)
       ========================= -->

  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Core OS: Upgrade Your Inner Operating System — Henrik Forrest</title>
  <meta name="description" content="Upgrade the system that runs you. A concise, practical playbook for executives, entrepreneurs, and rising professionals to debug defaults, install better habits, and ship clearer decisions." />

  <!-- Canonical -->
  <link rel="canonical" href="https://www.example.com/" /> <!-- TODO: replace with your domain -->

  <!-- Open Graph -->
  <meta property="og:type" content="product" />
  <meta property="og:title" content="Core OS: Upgrade Your Inner Operating System" />
  <meta property="og:description" content="A concise, practical playbook to upgrade the system that runs you." />
  <meta property="og:url" content="https://www.example.com/" /> <!-- TODO -->
  <meta property="og:image" content="https://www.example.com/assets/core-os-cover.jpg" /> <!-- TODO -->
  <meta property="product:brand" content="Henrik Forrest" />
  <meta property="product:availability" content="in stock" />
  <meta property="product:condition" content="new" />
  <meta property="product:price:amount" content="19.00" />
  <meta property="product:price:currency" content="USD" />

  <!-- Twitter Cards -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Core OS: Upgrade Your Inner Operating System" />
  <meta name="twitter:description" content="Upgrade your default code. Install better habits. Ship clearer decisions." />
  <meta name="twitter:image" content="https://www.example.com/assets/core-os-cover.jpg" />

  <!-- Favicon -->
  <link rel="icon" href="/assets/favicon.ico" /> <!-- TODO -->

  <!-- Minimal, modern CSS (no frameworks). Tailored for fast LCP and accessibility. -->
  <style>
    :root{
      --bg:#0b0d10;
      --bg-soft:#12151a;
      --card:#141821;
      --ink:#e9edf3;
      --muted:#aab3c2;
      --accent:#6ee7ff;
      --accent-2:#7fff9e;
      --shadow:rgba(0,0,0,.35);
      --radius:14px;
      --max:1120px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font:16px/1.5 system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif;
      color:var(--ink); background:radial-gradient(1200px 600px at 80% -10%, #1a2030 30%, #0b0d10 70%), var(--bg);
      -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
    }
    a{color:var(--accent); text-decoration:none}
    a:hover{text-decoration:underline}
    .wrap{max-width:var(--max); margin:0 auto; padding:clamp(16px,3vw,32px)}
    .nav{display:flex; align-items:center; justify-content:space-between; gap:16px; padding:14px 0}
    .brand{display:flex; align-items:center; gap:12px}
    .brand img{width:40px; height:40px; border-radius:10px; object-fit:cover}
    .brand b{font-weight:700; letter-spacing:.2px}
    .nav .links a{margin-left:18px; color:var(--muted)}
    .btn{
      display:inline-block; padding:14px 18px; border-radius:12px; background:linear-gradient(90deg,var(--accent),var(--accent-2));
      color:#041016; font-weight:700; border:0; box-shadow:0 8px 24px var(--shadow);
    }
    .btn:hover{text-decoration:none; transform:translateY(-1px)}
    .btn.secondary{
      background:transparent; color:var(--ink); border:1px solid #2d3442; box-shadow:none
    }
    .hero{display:grid; grid-template-columns:1.1fr .9fr; gap:32px; align-items:center; padding:32px 0 12px}
    .hero h1{font-size:clamp(28px,4.2vw,56px); line-height:1.05; margin:0 0 12px; letter-spacing:.2px}
    .hero p{color:var(--muted); margin:0 0 18px; font-size:clamp(16px,1.4vw,19px)}
    .badge{display:inline-flex; gap:8px; align-items:center; background:#0f131a; border:1px solid #222a36; padding:8px 12px; border-radius:999px; color:#b8c2d6; font-size:13px}
    .cover{
      background:linear-gradient(180deg,#1e2432,#111520);
      border:1px solid #2b3344; border-radius:18px; padding:16px; position:relative;
    }
    .cover img{width:100%; border-radius:12px; display:block; object-fit:cover}
    .grid-3{display:grid; grid-template-columns:repeat(3,1fr); gap:20px; margin:36px 0}
    .card{
      background:linear-gradient(180deg,#0f131a,#0b0d10);
      border:1px solid #1f2532; border-radius:var(--radius); padding:18px; box-shadow:0 6px 18px var(--shadow);
    }
    .card h3{margin:0 0 8px; font-size:18px}
    .meta{color:var(--muted); font-size:14px}
    .cta{display:flex; gap:12px; flex-wrap:wrap; margin:18px 0}
    .kpis{display:flex; gap:18px; flex-wrap:wrap; margin-top:8px}
    .kpis .chip{background:#0f131a; border:1px solid #222a36; padding:8px 12px; border-radius:999px; color:#c6d0e3; font-size:13px}
    .section{padding:48px 0}
    .section h2{font-size:26px; margin:0 0 16px}
    .logos{display:flex; gap:18px; flex-wrap:wrap; align-items:center; opacity:.9}
    .logos img{height:30px; filter:grayscale(1); opacity:.8}
    .testimonial{display:grid; grid-template-columns:80px 1fr; gap:14px; align-items:center}
    .testimonial img{width:80px; height:80px; border-radius:50%; object-fit:cover; border:1px solid #313a4a}
    .testimonial blockquote{margin:0; color:#dce4f5}
    .price{font-size:28px; font-weight:800}
    .cols{display:grid; grid-template-columns:1fr 1fr; gap:20px}
    .faq details{background:#0f131a; border:1px solid #1f2532; border-radius:12px; padding:14px 16px; margin-bottom:10px}
    .faq summary{font-weight:700; cursor:pointer}
    .footer{color:#8e99ad; border-top:1px solid #1f2532; padding:24px 0 60px}
    .footer a{color:#9fb5ff}
    .notice{font-size:13px; color:#8ea0b8}
    .skip-link{position:absolute; left:-9999px; top:auto; width:1px; height:1px; overflow:hidden}
    .skip-link:focus{position:static; width:auto; height:auto; padding:8px; background:#fff; color:#000; border-radius:6px}
    @media (max-width:980px){.hero{grid-template-columns:1fr}.grid-3{grid-template-columns:1fr}.cols{grid-template-columns:1fr}}
  </style>

  <!-- Schema.org JSON-LD (Book + Product) -->
  <script type="application/ld+json">
  {
    "@context":"https://schema.org",
    "@type":["Book","Product"],
    "name":"Core OS: Upgrade Your Inner Operating System",
    "author":{"@type":"Person","name":"Henrik Forrest"},
    "bookFormat":"https://schema.org/EBook",
    "inLanguage":"en",
    "image":"https://www.example.com/assets/core-os-cover.jpg",
    "description":"A practical playbook to debug defaults, install better habits, and ship clearer decisions.",
    "offers":{
      "@type":"Offer",
      "price":"19.00",
      "priceCurrency":"USD",
      "availability":"https://schema.org/InStock",
      "url":"https://buy.stripe.com/test_ABC123"  /* TODO: your Stripe Checkout link */
    }
  }
  </script>

  <!-- Optional privacy-friendly analytics (Plausible) -->
  <!-- <script defer data-domain="example.com" src="https://plausible.io/js/script.js"></script> -->
</head>
<body>
  <a class="skip-link" href="#main">Skip to content</a>

  <header class="wrap nav" role="banner">
    <div class="brand">
      <img src="/assets/hf-mark.png" alt="Henrik Forrest monogram"> <!-- TODO -->
      <b>Henrik Forrest</b>
    </div>
    <nav class="links" aria-label="Primary">
      <a href="#about">About</a>
      <a href="#inside">Inside the Book</a>
      <a href="#buy">Buy</a>
      <a href="#faq">FAQ</a>
    </nav>
  </header>

  <main id="main" class="wrap" role="main" aria-label="Core OS book">
    <section class="hero">
      <div>
        <span class="badge">✨ New Release</span>
        <h1>Core OS: <span aria-hidden="true">Upgrade Your Inner Operating System</span><span class="sr-only"</h1>
        <p>Upgrade the system that runs you. A concise, practical playbook for leaders who want clearer decisions, tighter habits, and a saner mind under load.</p>
        <div class="kpis">
          <span class="chip">≈ 95 pages</span>
          <span class="chip">Executives • Entrepreneurs • High-potential pros</span>
          <span class="chip">PDF • ePub • Kindle</span>
        </div>
        <div class="cta">
          <!-- Direct checkout (Stripe/Gumroad) -->
          <a class="btn" id="btn-direct" href="https://buy.stripe.com/test_ABC123?prefilled_purchased=true&utm_source=website&utm_medium=hero&utm_campaign=core_os_launch" rel="noopener" target="_blank">Buy Direct — $19</a>
          <!-- Marketplace hub -->
          <a class="btn secondary" href="#buy">See all stores</a>
          <!-- Sample chapter -->
          <a class="btn secondary" href="/assets/Core-OS_Sample-Chapter.pdf" download>Free Sample</a> <!-- TODO -->
        </div>
        <p class="notice">Secure checkout. Instant download. 30-day no-stress refund on direct purchases.</p>
      </div>
      <aside class="cover" aria-label="Book cover">
        <img src="/assets/core-os-cover.jpg" alt="Core OS book cover" />
      </aside>
    </section>

    <section id="inside" class="grid-3">
      <article class="card">
        <h3>Debug Your Defaults</h3>
        <p class="meta">Spot the hidden “code” behind your habits, attention, and decisions. Replace laggy loops with reliable routines.</p>
      </article>
      <article class="card">
        <h3>Install Better Habits</h3>
        <p class="meta">A lightweight framework to define, test, and lock in behaviors that actually survive busy seasons.</p>
      </article>
      <article class="card">
        <h3>Ship Clear Decisions</h3>
        <p class="meta">Decision filters, one-page reviews, and cadence templates to move from stall to ship.</p>
      </article>
    </section>

    <section id="about" class="section cols">
      <div class="card">
        <h2>About the Book</h2>
        <p><em>Core OS</em> is a focused, no-fluff system for leaders who don’t have time to read a 300-page pep talk. You’ll run a diagnostic, patch what’s noisy, and install a few powerful defaults—clarity, cadence, and calm execution.</p>
        <ul class="meta">
          <li>Printable worksheets + assessment</li>
          <li>Leadership-tested tools for high-stakes environments</li>
          <li>Designed to be re-read once a quarter</li>
        </ul>
      </div>
      <div class="card">
        <h2>What’s Inside</h2>
        <ul class="meta">
          <li>OS Diagnostic: surface bottlenecks and noisy loops</li>
          <li>Habit Installer: behavior spec → activation → lock-in</li>
          <li>Decision Filters: reduce rework and second-guessing</li>
          <li>Cadence Templates: weekly/quarterly reviews that don’t suck</li>
          <li>Reset Protocol: get back on track in 24 hours</li>
        </ul>
      </div>
    </section>

    <section class="section">
      <div class="card">
        <h2 id="buy">Buy the Book</h2>
        <p class="meta">Prefer your platform? Choose a store below or buy direct for instant PDF &amp; ePub.</p>
        <div class="cta">
          <!-- Direct -->
          <a class="btn" href="https://buy.stripe.com/test_ABC123?utm_source=website&utm_medium=buygrid&utm_campaign=core_os_launch" target="_blank" rel="noopener" data-platform="direct">Buy Direct</a>

          <!-- Marketplaces (use your real URLs) -->
          <a class="btn secondary" href="https://www.amazon.com/dp/ASIN?tag=henrikforrest-20&utm_source=site&utm_medium=btn&utm_campaign=core_os" target="_blank" rel="noopener" data-platform="amazon">Amazon</a>
          <a class="btn secondary" href="https://books.apple.com/book/idXXXXXXXXX?utm_source=site&utm_medium=btn&utm_campaign=core_os" target="_blank" rel="noopener" data-platform="apple">Apple Books</a>
          <a class="btn secondary" href="https://play.google.com/store/books/details?id=XXXXXXXXX&utm_source=site&utm_medium=btn&utm_campaign=core_os" target="_blank" rel="noopener" data-platform="google">Google Play</a>
          <a class="btn secondary" href="https://www.kobo.com/us/en/ebook/XXXXXXXX?utm_source=site&utm_medium=btn&utm_campaign=core_os" target="_blank" rel="noopener" data-platform="kobo">Kobo</a>
          <a class="btn secondary" href="https://www.barnesandnoble.com/w/XXXXXXXX/XXXXXXXX?utm_source=site&utm_medium=btn&utm_campaign=core_os" target="_blank" rel="noopener" data-platform="bn">Barnes &amp; Noble</a>
          <!-- Optional: Gumroad alternative -->
          <!-- <a class="btn" href="https://henrikforrest.gumroad.com/l/coreos" target="_blank" rel="noopener" data-platform="gumroad">Gumroad</a> -->
        </div>
        <p class="notice">Use code <b>UPGRADE10</b> at direct checkout for 10% off at launch.</p>
      </div>
    </section>

    <section class="section cols">
      <div class="card">
        <h2>Get a Sample Chapter</h2>
        <p class="meta">Drop your email for instant access + quarterly upgrade prompts. No spam, ever.</p>
        <!-- Formspree (replace with your endpoint) -->
        <form id="lead" action="https://formspree.io/f/your-id" method="POST" novalidate>
          <label for="email" class="sr-only">Email</label>
          <input id="email" type="email" name="email" required placeholder="you@work.com" aria-label="Email address"
                 style="width:100%;padding:14px 12px;border-radius:10px;border:1px solid #2b3444;background:#0c0f14;color:#e9edf3;margin-bottom:10px" />
          <button class="btn" type="submit">Send me the sample</button>
          <p id="lead-msg" class="notice" role="status" aria-live="polite" style="margin-top:8px;"></p>
        </form>
      </div>
      <div class="card">
        <h2>Share</h2>
        <p class="meta">Know a leader who’d appreciate a faster OS?</p>
        <div class="cta">
          <a class="btn secondary" href="#" id="share-x">Share on X</a>
          <a class="btn secondary" href="#" id="share-li">Share on LinkedIn</a>
          <a class="btn secondary" href="#" id="share-fb">Share on Facebook</a>
          <!-- Instagram doesn’t support web share—use the link-in-bio -->
          <a class="btn" href="https://www.example.com/?utm_source=instagram&utm_medium=bio&utm_campaign=core_os" target="_blank" rel="noopener">Link for Instagram Bio</a>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="card">
        <h2>Testimonials</h2>
        <div class="testimonial">
          <img src="/assets/avatar-exec1.jpg" alt="Photo of an executive reader"> <!-- TODO -->
          <blockquote>“A rare combo of clarity and practicality. We rolled this into our leadership cadence in a week.”</blockquote>
        </div>
        <div class="testimonial" style="margin-top:16px">
          <img src="/assets/avatar-founder1.jpg" alt="Photo of a founder reader">
          <blockquote>“Removed two decision bottlenecks and freed hours. My calendar and team both thank you.”</blockquote>
        </div>
      </div>
    </section>

    <section class="section cols">
      <div class="card">
        <h2>For Teams &amp; Enterprises</h2>
        <p class="meta">Bulk licensing, workshops, and leader kits available.</p>
        <a class="btn secondary" href="mailto:henrik@henrikforrest.com?subject=Core%20OS%20for%20Teams">Inquire</a> <!-- TODO -->
      </div>
      <div class="card">
        <h2>Specs</h2>
        <p class="meta">eBook (PDF &amp; ePub), ≈95 pages, includes printable worksheets. Lifetime updates for direct buyers.</p>
        <p class="price">$19</p>
      </div>
    </section>

    <section id="faq" class="section faq">
      <h2>FAQ</h2>
      <details>
        <summary>What formats do I get if I buy direct?</summary>
        <p class="meta">Instant PDF &amp; ePub downloads + any future minor updates.</p>
      </details>
      <details>
        <summary>Refunds?</summary>
        <p class="meta">30-day no-stress refund on direct purchases. Marketplaces follow their own policies.</p>
      </details>
      <details>
        <summary>Can I expense this?</summary>
        <p class="meta">Many readers do. You’ll receive an itemized receipt from Stripe/Gumroad.</p>
      </details>
    </section>
  </main>

  <footer class="wrap footer" role="contentinfo">
    <div style="display:flex;gap:18px;flex-wrap:wrap;align-items:center;justify-content:space-between">
      <small>© <span id="year"></span> Henrik Forrest. All rights reserved.</small>
      <div class="logos" aria-label="Retailer logos">
        <img src="/assets/logo-amazon.svg" alt="Amazon" />
        <img src="/assets/logo-applebooks.svg" alt="Apple Books" />
        <img src="/assets/logo-googleplay.svg" alt="Google Play Books" />
        <img src="/assets/logo-kobo.svg" alt="Kobo" />
        <img src="/assets/logo-bn.svg" alt="Barnes and Noble" />
      </div>
    </div>
    <p class="notice" style="margin-top:12px">
      <a href="/privacy.html">Privacy</a> · <a href="/terms.html">Terms</a> · <a href="mailto:hello@henrikforrest.com">Contact</a>
    </p>
  </footer>

  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Share links (replace domain if needed)
    const url = encodeURIComponent('https://www.example.com/');
    const text = encodeURIComponent('Core OS: Upgrade Your Inner Operating System');
    document.getElementById('share-x').href = `https://twitter.com/intent/tweet?url=${url}&text=${text}`;
    document.getElementById('share-li').href = `https://www.linkedin.com/sharing/share-offsite/?url=${url}`;
    document.getElementById('share-fb').href = `https://www.facebook.com/sharer/sharer.php?u=${url}`;

    // Lead form lightweight validation + friendly message
    const lead = document.getElementById('lead');
    const msg = document.getElementById('lead-msg');
    if (lead) {
      lead.addEventListener('submit', function(e){
        const email = document.getElementById('email').value.trim();
        if(!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)){
          e.preventDefault();
          msg.textContent = 'Please enter a valid email.';
          return false;
        }
        msg.textContent = 'Thanks! Check your inbox in a moment.';
      });
    }

    // Optional: smooth scroll for internal anchors
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id = a.getAttribute('href').slice(1);
        const el = document.getElementById(id);
        if(el){ e.preventDefault(); el.scrollIntoView({behavior:'smooth', block:'start'}); }
      });
    });
  </script>
</body>
</html>
