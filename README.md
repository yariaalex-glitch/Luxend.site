<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Luxend - Home</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: white;
      color: #003366; /* Aussie flag blue */
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #003366;
      color: white;
      padding: 20px;
      text-align: center;
      position: relative;
    }
    header img {
      max-height: 100px;
    }
    nav {
      position: absolute;
      top: 20px;
      right: 20px;
    }
    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      background: #003366;
      border-radius: 6px;
    }
    nav li {
      display: inline-block;
      margin: 0 10px;
    }
    nav a {
      text-decoration: none;
      color: gold;
      font-weight: bold;
    }
    .content {
      padding: 40px;
      text-align: center;
    }
    .quote {
      font-size: 1.3em;
      font-style: italic;
      margin-top: 20px;
      color: #cc9900; /* golden tone */
    }
  </style>
</head>
<body>
  <header>
    <img src="data:image/jpeg;base64,PUT_YOUR_LONG_BASE64_CODE_HERE" alt="Luxend Logo">
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Inquiries</a></li>
        <li><a href="#">Gallery</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">New Technologies</a></li>
        <li><a href="#">Products</a></li>
      </ul>
    </nav>
  </header>

  <div class="content">
    <h1>Welcome to Luxend</h1>
    <p>Luxend is a company that creates value for homes and properties by focusing on 
    high-quality materials and cost-effective, environmentally friendly solutions. 
    Our mission is to make homes more livable and provide a luxurious and happy life. 
    Founded by a highly educated team with several years of experience in construction 
    and the building industry, Luxend is dedicated to combining quality with innovative vision.</p>

    <p class="quote">“Luxend — for those looking for High-End living.”</p>
  </div>
</body>
</html>
4. Expanding to your 6 pages
You’d repeat this process for each page (Home, Inquiries, Gallery, About, New Technologies, Products), linking them together with proper file names (e.g., inquiries.html, gallery.html, etc.) and adjusting the <nav> links accordingly.

👉 Do you want me to generate the full set of six linked pages in one ready-to-use package (with your text, logo, and navigation), so you can just save and open them directly?







You said:
yes please


ChatGPT said:

Thought for 16s
awesome — here’s a complete, lightweight multi-page site for Luxend with a shared style + script and six linked pages.

How to use

Create a new folder named luxend-site.

Save the 8 files below into that folder (exact file names).

Save your logo image from above as luxend-logo.jpg in the same folder.

Double-click index.html to open the site.

1) styles.css
css
Copy code
:root{
  --lux-blue:#0a2a66;  /* Aussie-flag blue */
  --lux-gold:#c9a227;  /* soft gold accent */
  --ink:#122;
  --bg:#ffffff;
}

*{box-sizing:border-box}
html,body{margin:0;padding:0;background:var(--bg);color:var(--ink);font:16px/1.6 "Inter",system-ui,Segoe UI,Arial,sans-serif}
a{color:var(--lux-blue);text-decoration:none}
a:hover{text-decoration:underline}

.container{max-width:1100px;margin:0 auto;padding:24px}
.hero{
  background:linear-gradient(180deg,#fff 0%,#f7f9ff 100%);
  padding:56px 24px 72px;
  position:relative;
  overflow:hidden;
}
.hero::after{
  content:"";
  position:absolute;right:-80px;top:-80px;width:320px;height:320px;
  background:radial-gradient(closest-side,rgba(201,162,39,.18),transparent 70%);
  transform:rotate(12deg)
}

.brandbar{
  display:flex;align-items:center;justify-content:space-between;
  padding:12px 18px;border-bottom:1px solid #e7e9f3;background:#fff;position:sticky;top:0;z-index:10
}
.brand{
  display:flex;gap:12px;align-items:center
}
.brand img{height:48px;width:auto;border-radius:8px}
.brand h1{font-size:20px;letter-spacing:.06em;margin:0;color:var(--lux-blue)}
.tag{color:#345;opacity:.8;font-weight:500}

.btn{
  display:inline-block;padding:12px 18px;border-radius:999px;border:1px solid var(--lux-blue);
  background:#fff;color:var(--lux-blue);font-weight:600;box-shadow:0 2px 10px rgba(0,0,0,.04)
}
.btn.primary{background:var(--lux-blue);color:#fff;border-color:var(--lux-blue)}
.btn.gold{background:var(--lux-gold);border-color:var(--lux-gold);color:#111}
.btn:hover{filter:brightness(1.05)}

.grid{display:grid;gap:22px}
.grid.cols-3{grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
.card{
  background:#fff;border:1px solid #eef1f7;border-radius:18px;padding:22px;
  box-shadow:0 8px 24px rgba(10,42,102,.05)
}
.card h3{margin:0 0 8px;color:var(--lux-blue)}
.lead{font-size:18px;color:#223}
.quote{
  border-left:4px solid var(--lux-gold);padding:14px 16px;margin:16px 0;background:#fff8e6;border-radius:8px;color:#5a460e
}

footer{
  margin-top:56px;border-top:1px solid #eceff6;background:#fafcff;color:#456
}
.footer-inner{display:flex;gap:18px;justify-content:space-between;align-items:center;padding:18px}

.badge{
  display:inline-flex;align-items:center;gap:8px;border:1px solid #e6e8f2;border-radius:999px;padding:8px 12px;background:#fff
}

.hero .headline{font-size:36px;line-height:1.2;color:#0b2352;margin:0 0 10px;font-weight:800}
.hero .sub{max-width:840px;color:#334}
.ultralight{font-weight:300}
.highlight{color:var(--lux-gold);font-weight:700}

figure.thumb{margin:0;border-radius:16px;overflow:hidden;border:1px solid #edf0f7}
figure.thumb img{width:100%;height:200px;object-fit:cover;display:block}
figure.thumb figcaption{padding:12px 14px;background:#fff}

/* form / table style (Inquiries) */
table.form{width:100%;border-collapse:separate;border-spacing:0 10px}
table.form td:first-child{width:220px;color:#234;font-weight:600}
input[type="text"],input[type="email"],textarea{
  width:100%;padding:12px;border-radius:12px;border:1px solid #dfe5f2;background:#fff
}
small.muted{color:#789}

/* hamburger (top-right curtain) */
.menu{
  position:relative
}
.menu button{
  background:#fff;border:1px solid #dde3f2;border-radius:12px;padding:10px 12px;
  display:flex;flex-direction:column;gap:5px;cursor:pointer
}
.menu .bar{width:22px;height:2px;background:var(--lux-blue)}
.menu-panel{
  position:absolute;right:0;top:46px;background:#fff;border:1px solid #e3e8f5;border-radius:12px;
  min-width:220px;box-shadow:0 16px 40px rgba(0,0,0,.1);display:none
}
.menu-panel a{display:block;padding:12px 14px;border-bottom:1px solid #f0f3fa}
.menu-panel a:last-child{border-bottom:0}
.menu.open .menu-panel{display:block}

/* simple hero banner for inner pages */
.banner{
  background:linear-gradient(90deg,#0a2a66 0%,#123c8a 60%,#0a2a66 100%);
  color:#fff;padding:46px 24px
}

/* gallery modal */
.modal{
  position:fixed;inset:0;background:rgba(0,0,0,.55);display:none;align-items:center;justify-content:center;padding:20px;z-index:20
}
.modal.open{display:flex}
.modal-card{
  max-width:900px;background:#fff;border-radius:18px;overflow:hidden;border:1px solid #e7ecf7
}
.modal-media{max-height:420px;overflow:hidden}
.modal-media img{width:100%;height:100%;object-fit:cover;display:block}
.modal-body{padding:18px}
.modal-actions{display:flex;justify-content:flex-end;padding:12px 18px;border-top:1px solid #eff3fb;background:#fafcff}
2) script.js
javascript
Copy code
// hamburger toggle
document.addEventListener("click", (e)=>{
  const btn = e.target.closest("[data-menu-btn]");
  const menu = document.querySelector(".menu");
  if(btn){ menu.classList.toggle("open"); return; }
  if(!e.target.closest(".menu")) menu?.classList.remove("open");
});

// gallery modals (on gallery.html)
function openModal(id){
  const el = document.getElementById(id);
  if(el) el.classList.add("open");
}
function closeModal(el){
  el.closest(".modal")?.classList.remove("open");
}

// show contact info (on inquiries.html)
function revealContacts(){
  const box = document.getElementById("lux-contacts");
  box.hidden = !box.hidden;
}
3) partials.html
(Optional small include. If your editor doesn’t support includes, ignore this file. It just documents the shared header markup used in every page.)

html
Copy code
<!-- Shared Brandbar / Header (copied into each page) -->
<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div>
      <h1>LUXEND</h1>
      <div class="tag">High-end homes. Thoughtful simplicity.</div>
    </div>
  </div>

  <div class="menu">
    <button data-menu-btn aria-label="Open menu">
      <span class="bar"></span><span class="bar"></span><span class="bar"></span>
    </button>
    <div class="menu-panel">
      <a href="index.html">Home</a>
      <a href="inquiries.html">Inquiries</a>
      <a href="gallery.html">Gallery</a>
      <a href="about.html">About</a>
      <a href="technologies.html">New technologies</a>
      <a href="products.html">Products</a>
    </div>
  </div>
</div>
4) index.html (Home)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — Home</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<!-- Header / brand + hamburger -->
<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div>
      <h1>LUXEND</h1>
      <div class="tag">High-end homes. Thoughtful simplicity.</div>
    </div>
  </div>

  <div class="menu">
    <button data-menu-btn aria-label="Open menu">
      <span class="bar"></span><span class="bar"></span><span class="bar"></span>
    </button>
    <div class="menu-panel">
      <a href="index.html">Home</a>
      <a href="inquiries.html">Inquiries</a>
      <a href="gallery.html">Gallery</a>
      <a href="about.html">About</a>
      <a href="technologies.html">New technologies</a>
      <a href="products.html">Products</a>
    </div>
  </div>
</div>

<section class="hero">
  <div class="container">
    <p class="badge">Australian-inspired • Quality • Sustainability</p>
    <h2 class="headline">Creating value for homes & properties</h2>
    <p class="sub lead">
      At <strong>Luxend</strong>, our purpose is simple: make homes more livable and elevate daily life.
      We focus on <span class="highlight">high-quality materials</span> and
      <span class="highlight">cost-effective, environmentally friendly solutions</span> that bring
      a sense of luxury, calm, and happiness to every space.
    </p>
    <div style="margin:22px 0" class="quote">
      “<strong>Luxend</strong> — for those looking for a <em>High-end</em> life, or a more simple and inspiring path.”
    </div>
    <p class="lead ultralight">
      Our founding team is highly educated with years of construction and building experience. We don’t just build:
      we look into the <em>soul of the living environment</em> — crafting spaces where materials, light and landscape work together.
    </p>
    <div style="margin-top:24px">
      <a class="btn primary" href="inquiries.html">Start an inquiry</a>
      <a class="btn gold" href="gallery.html" style="margin-left:10px">Explore the gallery</a>
    </div>
  </div>
</section>

<div class="container">
  <div class="grid cols-3">
    <div class="card">
      <h3>Quality that lasts</h3>
      <p>Premium materials, careful detailing and verified suppliers—built for Australian conditions.</p>
    </div>
    <div class="card">
      <h3>Cost-effective & green</h3>
      <p>Design decisions that reduce lifecycle cost, energy and water use—without compromising aesthetics.</p>
    </div>
    <div class="card">
      <h3>Luxury with purpose</h3>
      <p>Comfort, calm, light and flow—spaces that feel sophisticated yet effortless every day.</p>
    </div>
  </div>
</div>

<footer>
  <div class="container footer-inner">
    <div>© <span id="y"></span> Luxend</div>
    <div class="tag">Blue • White • Gold</div>
  </div>
</footer>

<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
5) inquiries.html (Inquiries)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — Inquiries</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div><h1>LUXEND</h1><div class="tag">High-end homes. Thoughtful simplicity.</div></div>
  </div>
  <div class="menu">
    <button data-menu-btn aria-label="Open menu"><span class="bar"></span><span class="bar"></span><span class="bar"></span></button>
    <div class="menu-panel">
      <a href="index.html">Home</a><a href="inquiries.html">Inquiries</a><a href="gallery.html">Gallery</a>
      <a href="about.html">About</a><a href="technologies.html">New technologies</a><a href="products.html">Products</a>
    </div>
  </div>
</div>

<div class="banner"><div class="container"><h2>Start an inquiry</h2><p>Tell us a little about your project. We’ll get back to you shortly.</p></div></div>

<div class="container">
  <table class="form">
    <tr><td>Email address</td><td><input type="email" placeholder="name@example.com"></td></tr>
    <tr><td>Name</td><td><input type="text" placeholder="Your full name"></td></tr>
    <tr><td>Subject of inquiry</td><td><input type="text" placeholder="e.g., Renovation, New build, Landscaping"></td></tr>
    <tr><td>Australian phone number</td><td><input type="text" placeholder="+61 ..."></td></tr>
    <tr><td>Details (up to ~1500 words)</td><td><textarea rows="8" placeholder="Tell us about your ideas, goals, budget range, and timeline."></textarea></td></tr>
  </table>

  <p><a href="javascript:void(0)" onclick="revealContacts()">Click to reveal Luxend direct email & phone</a></p>
  <div id="lux-contacts" hidden class="card">
    <strong>Email:</strong> <!-- add later --> <br>
    <strong>Phone:</strong> <!-- add later -->
    <p class="small muted"><small>Contact details intentionally left blank for now — replace here anytime.</small></p>
  </div>
</div>

<footer><div class="container footer-inner"><div>© <span id="y"></span> Luxend</div></div></footer>
<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
6) gallery.html (Gallery with 6 picture links + modals)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — Gallery</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div><h1>LUXEND</h1><div class="tag">High-end homes. Thoughtful simplicity.</div></div>
  </div>
  <div class="menu">
    <button data-menu-btn aria-label="Open menu"><span class="bar"></span><span class="bar"></span><span class="bar"></span></button>
    <div class="menu-panel">
      <a href="index.html">Home</a><a href="inquiries.html">Inquiries</a><a href="gallery.html">Gallery</a>
      <a href="about.html">About</a><a href="technologies.html">New technologies</a><a href="products.html">Products</a>
    </div>
  </div>
</div>

<div class="banner"><div class="container"><h2>Gallery</h2><p>Minimal, luxurious inspiration across design, facade, colour, terrain, landscaping and development.</p></div></div>

<div class="container grid cols-3">

  <a href="javascript:void(0)" onclick="openModal('m1')" aria-label="Design of your dream home">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Design your dream home</strong></figcaption>
    </figure>
  </a>

  <a href="javascript:void(0)" onclick="openModal('m2')" aria-label="Facade">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Facade options</strong></figcaption>
    </figure>
  </a>

  <a href="javascript:void(0)" onclick="openModal('m3')" aria-label="Colour & painting">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1493809842364-78817add7ffb?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Colour & painting</strong></figcaption>
    </figure>
  </a>

  <a href="javascript:void(0)" onclick="openModal('m4')" aria-label="Slopes & cliffs">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1526404079162-8f4f0f5f1c86?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Geotechnical solutions</strong></figcaption>
    </figure>
  </a>

  <a href="javascript:void(0)" onclick="openModal('m5')" aria-label="Landscaping">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1532372320978-9b1d4e55b5a3?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Landscaping inspiration</strong></figcaption>
    </figure>
  </a>

  <a href="javascript:void(0)" onclick="openModal('m6')" aria-label="Development & subdivision">
    <figure class="thumb">
      <img src="https://images.unsplash.com/photo-1600607687920-4ce664d11078?q=80&w=1200&auto=format&fit=crop" alt="">
      <figcaption><strong>Development & subdivision</strong></figcaption>
    </figure>
  </a>
</div>

<!-- Modals -->
<div class="modal" id="m1">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Design of your dream home</h3>
      <p>We design from your imagination outward—capturing mood, light, flow and functionality. The result is a luxurious, minimal home tailored to Australian living, with refined materials and calm proportions.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<div class="modal" id="m2">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Facade choices</h3>
      <p>Choose a refreshed renovation or a brand-new facade concept. Options include: contemporary coastal (light render, timber accents), urban brick with refined mortar, or sculpted cement panels with warm metallic trims.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<div class="modal" id="m3">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1493809842364-78817add7ffb?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Colour & painting</h3>
      <p>Colour shapes mood. We specify palettes and premium coatings for interiors and exteriors—walls, roofs, balustrades and fences, doors and trims—guided by specialists to achieve durability and an elegant finish.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<div class="modal" id="m4">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1526404079162-8f4f0f5f1c86?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Geotechnical & sloped sites</h3>
      <p>Challenging sites—slopes, cliffs and complex ground—are opportunities. We combine geotechnical design with architecture to deliver secure foundations, dramatic outlooks and truly unique homes that turn terrain into a masterpiece.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<div class="modal" id="m5">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1564540587553-852d9c1d0f3b?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Landscaping</h3>
      <p>Front and backyard concepts that lift value and make neighbours jealous—in a nice way. Minimal design with succulents, white sands, native textures and sculptural lighting for a timeless Australian aesthetic.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<div class="modal" id="m6">
  <div class="modal-card">
    <div class="modal-media"><img src="https://images.unsplash.com/photo-1600607687920-4ce664d11078?q=80&w=2000&auto=format&fit=crop" alt=""></div>
    <div class="modal-body">
      <h3>Development & subdivision</h3>
      <p>From feasibility to design, we advise on land development and subdivision to maximise value—townhouses that feel premium and distinctly Australian, with efficient use of land and refined street presence.</p>
    </div>
    <div class="modal-actions"><a class="btn" onclick="closeModal(this)">Close</a></div>
  </div>
</div>

<footer><div class="container footer-inner"><div>© <span id="y"></span> Luxend</div></div></footer>
<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
7) about.html (About)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — About</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div><h1>LUXEND</h1><div class="tag">High-end homes. Thoughtful simplicity.</div></div>
  </div>
  <div class="menu">
    <button data-menu-btn aria-label="Open menu"><span class="bar"></span><span class="bar"></span><span class="bar"></span></button>
    <div class="menu-panel">
      <a href="index.html">Home</a><a href="inquiries.html">Inquiries</a><a href="gallery.html">Gallery</a>
      <a href="about.html">About</a><a href="technologies.html">New technologies</a><a href="products.html">Products</a>
    </div>
  </div>
</div>

<div class="banner"><div class="container"><h2>About Luxend</h2></div></div>

<div class="container grid cols-3">
  <div class="card" style="grid-column:1/-1">
    <h3>Founder</h3>
    <p><strong>Alex Yari</strong> founded Luxend with a clear vision: combine new materials, environmentally friendly solutions and a luxury-minded approach to design. He holds a PhD in materials from Deakin University, has a strong background in civil and the building industry, broad international experience, and an Australian Building Licence. This combination shapes a practical, innovative view that brings genuine value to homes and properties.</p>
  </div>

  <div class="card">
    <h3>Material intelligence</h3>
    <p>We evaluate materials for performance, durability and beauty—specifying what suits Australian climates and life.</p>
  </div>
  <div class="card">
    <h3>Design with soul</h3>
    <p>Light, proportion and texture are tuned to feel calm and luxurious—minimal yet warm, timeless rather than trendy.</p>
  </div>
  <div class="card">
    <h3>A highly educated team</h3>
    <p>Our team members bring strong academic backgrounds and deep industry experience across design, engineering and delivery.</p>
  </div>
</div>

<footer><div class="container footer-inner"><div>© <span id="y"></span> Luxend</div></div></footer>
<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
8) technologies.html (New technologies)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — New Technologies</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div><h1>LUXEND</h1><div class="tag">High-end homes. Thoughtful simplicity.</div></div>
  </div>
  <div class="menu">
    <button data-menu-btn aria-label="Open menu"><span class="bar"></span><span class="bar"></span><span class="bar"></span></button>
    <div class="menu-panel">
      <a href="index.html">Home</a><a href="inquiries.html">Inquiries</a><a href="gallery.html">Gallery</a>
      <a href="about.html">About</a><a href="technologies.html">New technologies</a><a href="products.html">Products</a>
    </div>
  </div>
</div>

<div class="banner"><div class="container"><h2>Smart, efficient & safe</h2></div></div>

<div class="container grid cols-3">

  <div class="card" style="grid-column:1/-1">
    <p>Luxend curates new technologies for comfort and efficiency—lighting control, solar-panel integration, and intelligent water & heat management. We assess payback periods, maintenance and user experience to ensure each solution genuinely improves life at home.</p>
    <p>We design smart-home systems that are simple to use: scenes for evening, away-from-home automation, and silent background energy savings with quality hardware and clean wiring.</p>
    <p>Safety matters: our alarm choices include security sensors, smart locks, CCTV integration, and fire/smoke detection tied into your system—tested, monitored and easy to expand.</p>
  </div>

  <figure class="thumb">
    <img src="https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?q=80&w=1200&auto=format&fit=crop" alt="">
    <figcaption>Smart lighting & scenes</figcaption>
  </figure>

  <figure class="thumb">
    <img src="https://images.unsplash.com/photo-1509395176047-4a66953fd231?q=80&w=1200&auto=format&fit=crop" alt="">
    <figcaption>Solar & energy systems</figcaption>
  </figure>

  <figure class="thumb">
    <img src="https://images.unsplash.com/photo-1558002038-1055907df827?q=80&w=1200&auto=format&fit=crop" alt="">
    <figcaption>Security & fire detection</figcaption>
  </figure>

</div>

<footer><div class="container footer-inner"><div>© <span id="y"></span> Luxend</div></div></footer>
<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
9) products.html (Products overview with links)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Luxend — Products</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="brandbar">
  <div class="brand">
    <img src="luxend-logo.jpg" alt="Luxend logo">
    <div><h1>LUXEND</h1><div class="tag">High-end homes. Thoughtful simplicity.</div></div>
  </div>
  <div class="menu">
    <button data-menu-btn aria-label="Open menu"><span class="bar"></span><span class="bar"></span><span class="bar"></span></button>
    <div class="menu-panel">
      <a href="index.html">Home</a><a href="inquiries.html">Inquiries</a><a href="gallery.html">Gallery</a>
      <a href="about.html">About</a><a href="technologies.html">New technologies</a><a href="products.html">Products</a>
    </div>
  </div>
</div>

<div class="banner"><div class="container"><h2>Products & Services</h2><p>Luxend’s curated offerings—coherent with our blue, white and gold palette and minimal aesthetic.</p></div></div>

<div class="container grid cols-3">

  <a class="card" href="gallery.html#m3">
    <h3>Paint</h3>
    <p>Premium coatings, colour schedules, interior & exterior systems.</p>
  </a>

  <a class="card" href="gallery.html#m5">
    <h3>Landscaping products</h3>
    <p>Minimal, luxury selections for Australian front & back yards.</p>
  </a>

  <a class="card" href="technologies.html">
    <h3>Smart home solutions</h3>
    <p>Lighting, solar, water & heat control, security and fire/smoke systems.</p>
  </a>

  <a class="card" href="inquiries.html">
    <h3>Demolish solutions</h3>
    <p>Safe, efficient pre-build strategies and council-aligned process.</p>
  </a>

  <a class="card" href="inquiries.html">
    <h3>Brand-new design & build</h3>
    <p>From feasibility to handover—architecture, engineering and delivery.</p>
  </a>

  <a class="card" href="gallery.html#m1">
    <h3>Designs</h3>
    <p>Bespoke plans and elevations tuned to your lifestyle and site.</p>
  </a>

</div>

<footer><div class="container footer-inner"><div>© <span id="y"></span> Luxend</div></div></footer>
<script src="script.js"></script>
<script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
