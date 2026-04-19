# andresrsdz-rgb.gitbub.io
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ChileSeating — El mayor instalador de butacas en Chile</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --gold:#C9A84C;--dark:#0D0D0D;--charcoal:#1A1A1A;--mid:#2E2E2E;
  --light:#F5F2EE;--lighter:#FAFAF8;--text:#1A1A1A;--muted:#6B6360;
  --border:rgba(0,0,0,0.08);--gold-light:#F0E6C8;
}
body{font-family:'DM Sans',sans-serif;background:var(--lighter);color:var(--text);overflow-x:hidden;scroll-behavior:smooth}

nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(13,13,13,0.96);backdrop-filter:blur(10px);padding:0 5%;height:64px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid rgba(201,168,76,0.2)}
.nav-logo{font-family:'Playfair Display',serif;color:#fff;font-size:22px;font-weight:700;letter-spacing:0.04em}
.nav-logo span{color:var(--gold)}
.nav-links{display:flex;gap:32px;list-style:none}
.nav-links a{color:rgba(255,255,255,0.7);text-decoration:none;font-size:13px;letter-spacing:0.08em;text-transform:uppercase;transition:color 0.2s}
.nav-links a:hover{color:var(--gold)}
.nav-cta{background:var(--gold);color:var(--dark);padding:10px 24px;font-size:13px;font-weight:500;border:none;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;font-family:'DM Sans',sans-serif}
.nav-cta:hover{opacity:0.88}

.hero{min-height:100vh;background:var(--dark);position:relative;display:flex;align-items:center;overflow:hidden}
.hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse at 70% 50%,rgba(201,168,76,0.08) 0%,transparent 60%)}
.hero-grid{position:absolute;inset:0;opacity:0.025;background-image:linear-gradient(rgba(255,255,255,0.5) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,0.5) 1px,transparent 1px);background-size:60px 60px}
.hero-content{position:relative;z-index:2;padding:0 5%;max-width:700px;margin-top:64px}
.hero-tag{display:inline-block;background:rgba(201,168,76,0.15);border:1px solid rgba(201,168,76,0.3);color:var(--gold);font-size:11px;letter-spacing:0.14em;text-transform:uppercase;padding:6px 16px;margin-bottom:28px}
.hero h1{font-family:'Playfair Display',serif;color:#fff;font-size:clamp(44px,5.5vw,80px);line-height:1.1;font-weight:900;margin-bottom:24px}
.hero h1 em{color:var(--gold);font-style:normal}
.hero-sub{color:rgba(255,255,255,0.55);font-size:17px;line-height:1.7;max-width:500px;margin-bottom:40px;font-weight:300}
.hero-actions{display:flex;gap:16px;align-items:center;flex-wrap:wrap}
.btn-primary{background:var(--gold);color:var(--dark);padding:14px 32px;font-weight:500;font-size:14px;letter-spacing:0.06em;text-transform:uppercase;border:none;cursor:pointer;transition:opacity 0.2s;font-family:'DM Sans',sans-serif}
.btn-primary:hover{opacity:0.88}
.btn-ghost{background:transparent;color:rgba(255,255,255,0.7);padding:14px 32px;font-size:14px;letter-spacing:0.06em;text-transform:uppercase;border:1px solid rgba(255,255,255,0.2);cursor:pointer;transition:all 0.2s;font-family:'DM Sans',sans-serif}
.btn-ghost:hover{border-color:var(--gold);color:var(--gold)}
.hero-stats{position:absolute;right:5%;bottom:60px;display:flex;gap:40px;z-index:2}
.stat{text-align:right}
.stat-num{font-family:'Playfair Display',serif;color:#fff;font-size:36px;font-weight:700}
.stat-num sup{color:var(--gold);font-size:18px;vertical-align:super}
.stat-label{color:rgba(255,255,255,0.35);font-size:11px;letter-spacing:0.1em;text-transform:uppercase;margin-top:2px}

section{padding:100px 5%}
.section-tag{display:inline-block;color:var(--gold);font-size:11px;letter-spacing:0.16em;text-transform:uppercase;margin-bottom:16px;font-weight:500}
.section-title{font-family:'Playfair Display',serif;font-size:clamp(32px,4vw,52px);font-weight:700;line-height:1.15;margin-bottom:20px}
.section-sub{color:var(--muted);font-size:16px;line-height:1.7;max-width:520px;font-weight:300}
.divider{width:48px;height:2px;background:var(--gold);margin:24px 0}

.categories{background:var(--lighter)}
.cat-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:56px;flex-wrap:wrap;gap:24px}
.cat-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:2px;background:rgba(0,0,0,0.06)}
.cat-card{background:#fff;padding:40px 32px;position:relative;overflow:hidden;cursor:pointer;transition:transform 0.3s}
.cat-card:hover{transform:translateY(-4px)}
.cat-card::after{content:'';position:absolute;bottom:0;left:0;right:0;height:3px;background:var(--gold);transform:scaleX(0);transform-origin:left;transition:transform 0.3s}
.cat-card:hover::after{transform:scaleX(1)}
.cat-emoji{font-size:36px;margin-bottom:20px;display:block}
.cat-name{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;margin-bottom:12px}
.cat-desc{color:var(--muted);font-size:14px;line-height:1.65;margin-bottom:20px}
.cat-count{font-size:11px;color:var(--gold);letter-spacing:0.1em;text-transform:uppercase;font-weight:500}
.cat-arrow{position:absolute;top:32px;right:32px;width:32px;height:32px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--muted);font-size:16px;transition:all 0.2s}
.cat-card:hover .cat-arrow{background:var(--gold);border-color:var(--gold);color:var(--dark)}

.why{background:var(--dark);color:#fff}
.why .section-title{color:#fff}
.why-grid{display:grid;grid-template-columns:1fr 1fr;gap:0;margin-top:60px}
.why-item{padding:40px;border:1px solid rgba(255,255,255,0.06);position:relative;transition:background 0.2s}
.why-item:hover{background:rgba(201,168,76,0.04)}
.why-num{font-family:'Playfair Display',serif;font-size:64px;font-weight:900;color:rgba(201,168,76,0.1);line-height:1;position:absolute;top:24px;right:28px}
.why-dot{width:8px;height:8px;background:var(--gold);border-radius:50%;margin-bottom:20px}
.why-title{font-size:18px;font-weight:500;margin-bottom:12px;color:#fff}
.why-text{color:rgba(255,255,255,0.45);font-size:14px;line-height:1.7;font-weight:300}

.projects{background:var(--lighter)}
.proj-filter{display:flex;gap:8px;margin-bottom:48px;flex-wrap:wrap}
.filter-btn{padding:8px 20px;font-size:12px;letter-spacing:0.08em;text-transform:uppercase;border:1px solid var(--border);background:transparent;cursor:pointer;color:var(--muted);transition:all 0.2s;font-weight:500;font-family:'DM Sans',sans-serif}
.filter-btn.active,.filter-btn:hover{background:var(--dark);color:#fff;border-color:var(--dark)}
.proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:3px}
.proj-card{position:relative;overflow:hidden;aspect-ratio:4/3;cursor:pointer}
.proj-inner{width:100%;height:100%;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:10px;transition:transform 0.5s}
.proj-card:hover .proj-inner{transform:scale(1.06)}
.proj-emoji{font-size:56px}
.proj-units{font-size:11px;letter-spacing:0.1em;text-transform:uppercase;opacity:0.7;font-weight:500}
.proj-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,0.88) 0%,transparent 55%);opacity:0;transition:opacity 0.3s;display:flex;align-items:flex-end;padding:24px}
.proj-card:hover .proj-overlay{opacity:1}
.proj-tag{font-size:10px;letter-spacing:0.12em;text-transform:uppercase;color:var(--gold);margin-bottom:6px;font-weight:500}
.proj-name{color:#fff;font-family:'Playfair Display',serif;font-size:18px;font-weight:700;line-height:1.2}
.proj-detail{color:rgba(255,255,255,0.55);font-size:12px;margin-top:4px}
.proj-footer{position:absolute;bottom:0;left:0;right:0;padding:16px 20px;background:linear-gradient(to top,rgba(0,0,0,0.65),transparent)}
.proj-footer-name{color:#fff;font-size:13px;font-weight:500}
.proj-footer-tag{color:var(--gold);font-size:10px;letter-spacing:0.1em;text-transform:uppercase}

.testimonials{background:#fff}
.test-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:2px;background:rgba(0,0,0,0.06);margin-top:60px}
.test-card{background:#fff;padding:36px}
.test-quote{font-family:'Playfair Display',serif;font-size:64px;color:var(--gold);line-height:0.7;margin-bottom:20px;opacity:0.35}
.test-text{color:var(--text);font-size:15px;line-height:1.7;margin-bottom:24px;font-style:italic;font-weight:300}
.test-author{display:flex;align-items:center;gap:12px}
.test-avatar{width:40px;height:40px;background:var(--gold-light);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:700;color:var(--gold);font-family:'Playfair Display',serif;flex-shrink:0}
.test-name{font-size:14px;font-weight:500}
.test-role{font-size:12px;color:var(--muted)}

.cta-wrap{background:var(--charcoal);padding:100px 5%;text-align:center;position:relative;overflow:hidden}
.cta-wrap::before{content:'';position:absolute;inset:0;background:radial-gradient(ellipse at 50% 120%,rgba(201,168,76,0.12) 0%,transparent 60%)}
.cta-wrap .section-title{color:#fff;text-align:center;margin-bottom:20px}
.cta-sub{color:rgba(255,255,255,0.5);font-size:16px;max-width:480px;margin:0 auto 40px;line-height:1.7;font-weight:300}
.cta-actions{display:flex;gap:16px;justify-content:center;flex-wrap:wrap}

.contact{background:var(--lighter)}
.contact-wrap{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:start}
.contact-form{display:flex;flex-direction:column;gap:16px}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.form-group{display:flex;flex-direction:column;gap:6px}
.form-label{font-size:11px;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);font-weight:500}
.form-input,.form-select,.form-textarea{background:#fff;border:1px solid rgba(0,0,0,0.12);padding:12px 16px;font-size:14px;font-family:'DM Sans',sans-serif;color:var(--text);outline:none;transition:border-color 0.2s;-webkit-appearance:none}
.form-input:focus,.form-select:focus,.form-textarea:focus{border-color:var(--gold)}
.form-textarea{resize:vertical;min-height:100px}
.form-submit{background:var(--gold);color:var(--dark);padding:14px 32px;border:none;font-size:13px;letter-spacing:0.1em;text-transform:uppercase;cursor:pointer;font-weight:500;font-family:'DM Sans',sans-serif;margin-top:8px;transition:opacity 0.2s;align-self:flex-start}
.form-submit:hover{opacity:0.85}
.contact-item{display:flex;gap:16px;margin-bottom:28px;align-items:flex-start}
.contact-ico{width:44px;height:44px;background:var(--gold-light);display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
.contact-lbl{font-weight:500;font-size:14px;margin-bottom:3px}
.contact-val{color:var(--muted);font-size:14px}
.showrooms{margin-top:36px;padding-top:28px;border-top:1px solid var(--border)}
.showrooms-title{font-size:11px;letter-spacing:0.12em;text-transform:uppercase;color:var(--muted);margin-bottom:14px;font-weight:500}
.showroom{background:#fff;padding:14px 18px;border:1px solid var(--border);margin-bottom:8px}
.showroom-name{font-size:14px;font-weight:500}
.showroom-addr{font-size:13px;color:var(--muted);margin-top:2px}
.success-box{display:none;padding:24px;background:#F0FAF0;border:1px solid #A5D6A7;margin-top:16px}
.success-box h4{color:#2E7D32;font-weight:500;margin-bottom:4px}
.success-box p{color:#388E3C;font-size:13px}

footer{background:var(--dark);color:rgba(255,255,255,0.3);text-align:center;padding:32px 5%;font-size:12px;letter-spacing:0.04em}
footer a{color:var(--gold);text-decoration:none}
footer p+p{margin-top:8px}

.split-header{display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:end;margin-bottom:56px}

@media(max-width:768px){
  .hero-stats{position:relative;right:auto;bottom:auto;margin-top:48px;flex-wrap:wrap;gap:24px;justify-content:flex-start}
  .why-grid,.contact-wrap,.split-header,.form-row{grid-template-columns:1fr}
  .nav-links{display:none}
}
</style>
</head>
<body>

<nav>
  <div class="nav-logo">Chile<span>Seating</span></div>
  <ul class="nav-links">
    <li><a href="#productos">Productos</a></li>
    <li><a href="#proyectos">Proyectos</a></li>
    <li><a href="#nosotros">Nosotros</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
  <button class="nav-cta" onclick="document.getElementById('contacto').scrollIntoView({behavior:'smooth'})">Cotizar Proyecto</button>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div class="hero-tag">El mayor instalador de butacas en Chile</div>
    <h1>Cada <em>espacio</em><br>merece una<br>butaca <em>excepcional</em></h1>
    <p class="hero-sub">Diseñamos, fabricamos e instalamos butacas para teatros, estadios, auditorios y centros culturales. Más de 60 modelos personalizables para hacer de su proyecto algo único.</p>
    <div class="hero-actions">
      <button class="btn-primary" onclick="document.getElementById('productos').scrollIntoView({behavior:'smooth'})">Ver Catálogo</button>
      <button class="btn-ghost" onclick="document.getElementById('proyectos').scrollIntoView({behavior:'smooth'})">Obras Realizadas</button>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-num">+30<sup>años</sup></div>
        <div class="stat-label">En el mercado</div>
      </div>
      <div class="stat">
        <div class="stat-num">+60</div>
        <div class="stat-label">Modelos</div>
      </div>
      <div class="stat">
        <div class="stat-num">#1</div>
        <div class="stat-label">Instalador nacional</div>
      </div>
    </div>
  </div>
</section>

<!-- PRODUCTOS -->
<section class="categories" id="productos">
  <div class="cat-header">
    <div>
      <div class="section-tag">Nuestros Productos</div>
      <h2 class="section-title">Soluciones para<br>cada espacio</h2>
      <div class="divider"></div>
    </div>
    <p class="section-sub">Desde íconos culturales hasta estadios de primer nivel. Cada butaca libre de mantención, con garantía local de reposición.</p>
  </div>
  <div class="cat-grid">
    <div class="cat-card">
      <div class="cat-arrow">→</div>
      <span class="cat-emoji">🎭</span>
      <div class="cat-name">Teatros & Auditorios</div>
      <div class="cat-desc">Modelos Granada, París, Bruselas y más. Tapicería premium, maderas nobles, numeración personalizada. Para espacios donde cada detalle importa.</div>
      <div class="cat-count">Granada · París · Bruselas · Resende</div>
    </div>
    <div class="cat-card">
      <div class="cat-arrow">→</div>
      <span class="cat-emoji">🏟</span>
      <div class="cat-name">Estadios & Deportivos</div>
      <div class="cat-desc">Monocasco, Aconcagua y butacas con espaldar. Diseño aprobado por FIFA, resistencia UV, sistema de drenaje integrado para uso intensivo.</div>
      <div class="cat-count">Monocasco · Aconcagua · Espaldar</div>
    </div>
    <div class="cat-card">
      <div class="cat-arrow">→</div>
      <span class="cat-emoji">🪑</span>
      <div class="cat-name">Salas de Conferencia</div>
      <div class="cat-desc">Modelo Minor abatible con sistema Tandem. Solo 18 cm plegado. Ideal para recintos multifuncionales que requieren máxima versatilidad.</div>
      <div class="cat-count">Minor · Sistema Tandem · Plegable</div>
    </div>
    <div class="cat-card">
      <div class="cat-arrow">→</div>
      <span class="cat-emoji">✦</span>
      <div class="cat-name">Personalización Total</div>
      <div class="cat-desc">Bordado, pirograbado, bajorrelieve, tapicería única. Dimensiones, maderas, colores y accesorios completamente a medida para cada proyecto.</div>
      <div class="cat-count">+60 combinaciones · Colores Pantone</div>
    </div>
  </div>
</section>

<!-- POR QUÉ -->
<section class="why" id="nosotros">
  <div class="section-tag">¿Por qué elegirnos?</div>
  <h2 class="section-title" style="color:#fff">La única empresa<br>exclusivamente dedicada<br>a <em style="color:var(--gold);font-style:normal">este rubro</em> en Chile</h2>
  <div class="why-grid">
    <div class="why-item">
      <div class="why-num">01</div>
      <div class="why-dot"></div>
      <div class="why-title">Especialización única</div>
      <div class="why-text">Somos la única empresa en Chile dedicada exclusivamente a butacas para recintos. Sin distracciones, sin compromisos: solo la mejor butaca posible para su proyecto.</div>
    </div>
    <div class="why-item">
      <div class="why-num">02</div>
      <div class="why-dot"></div>
      <div class="why-title">Mayor instalador del país</div>
      <div class="why-text">Décadas de experiencia nos posicionan como el instalador número uno de Chile. Hemos equipado teatros emblemáticos, universidades, estadios y centros culturales a lo largo de todo el territorio.</div>
    </div>
    <div class="why-item">
      <div class="why-num">03</div>
      <div class="why-dot"></div>
      <div class="why-title">Cero mantención</div>
      <div class="why-text">Materiales sólidos y resistentes para uso intensivo. Garantía local de reposición que asegura la durabilidad de su inversión a largo plazo sin costos adicionales.</div>
    </div>
    <div class="why-item">
      <div class="why-num">04</div>
      <div class="why-dot"></div>
      <div class="why-title">Compromiso sustentable</div>
      <div class="why-text">Promovemos prácticas sustentables mediante el reciclaje de butacas antiguas. Porque cuidar el espacio donde nos sentamos es también cuidar el planeta.</div>
    </div>
  </div>
</section>

<!-- PROYECTOS -->
<section class="projects" id="proyectos">
  <div class="split-header">
    <div>
      <div class="section-tag">Obras Realizadas</div>
      <h2 class="section-title">Chile de norte<br>a sur, sentado<br>en <em style="color:var(--gold);font-style:normal">ChileSeating</em></h2>
    </div>
    <p class="section-sub" style="align-self:end">Desde el Teatro Municipal de Iquique hasta centros culturales en la Araucanía. Cada instalación es un testimonio de calidad y precisión.</p>
  </div>

  <div class="proj-filter">
    <button class="filter-btn active" onclick="filterProj('all',this)">Todos</button>
    <button class="filter-btn" onclick="filterProj('teatro',this)">Teatros</button>
    <button class="filter-btn" onclick="filterProj('universidad',this)">Universidades</button>
    <button class="filter-btn" onclick="filterProj('cultural',this)">Centros Culturales</button>
    <button class="filter-btn" onclick="filterProj('estadio',this)">Estadios</button>
  </div>
  <div class="proj-grid" id="projGrid"></div>
</section>

<!-- TESTIMONIOS -->
<section class="testimonials">
  <div class="section-tag">Testimonios</div>
  <h2 class="section-title">Lo que dicen<br>los arquitectos</h2>
  <div class="test-grid">
    <div class="test-card">
      <div class="test-quote">"</div>
      <p class="test-text">La calidad de los materiales y la precisión en la instalación superaron nuestras expectativas. El resultado final fue exactamente la atmósfera que buscábamos para el auditorio.</p>
      <div class="test-author">
        <div class="test-avatar">PS</div>
        <div>
          <div class="test-name">Arq. Plane Studio</div>
          <div class="test-role">Estudio de Arquitectura</div>
        </div>
      </div>
    </div>
    <div class="test-card">
      <div class="test-quote">"</div>
      <p class="test-text">La personalización que ofrecen es incomparable. Pudimos diseñar butacas que complementaron perfectamente el lenguaje arquitectónico del proyecto sin sacrificar el confort.</p>
      <div class="test-author">
        <div class="test-avatar">BA</div>
        <div>
          <div class="test-name">Arq. BiS Arquitectos Ltda.</div>
          <div class="test-role">Arquitectura & Diseño</div>
        </div>
      </div>
    </div>
    <div class="test-card">
      <div class="test-quote">"</div>
      <p class="test-text">Trabajamos con ellos en la restauración del Teatro de Lota. Las 813 butacas instaladas respetan el espíritu Art Déco del recinto mientras ofrecen confort moderno. Un trabajo impecable.</p>
      <div class="test-author">
        <div class="test-avatar">IM</div>
        <div>
          <div class="test-name">Arq. Isabel Martínez</div>
          <div class="test-role">Teatro Chiflón del Diablo, Lota</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-wrap">
  <div style="position:relative;z-index:2">
    <div class="section-tag" style="display:block;text-align:center;margin-bottom:16px">Su próximo proyecto</div>
    <h2 class="section-title" style="color:#fff;text-align:center">¿Tiene un proyecto<br>en mente?</h2>
    <p class="cta-sub">Nuestros especialistas le asesoran desde la etapa de diseño arquitectónico hasta la instalación final. Respuesta ágil garantizada.</p>
    <div class="cta-actions">
      <button class="btn-primary" onclick="document.getElementById('contacto').scrollIntoView({behavior:'smooth'})">Solicitar Cotización</button>
      <button class="btn-ghost" onclick="document.getElementById('productos').scrollIntoView({behavior:'smooth'})">Ver Catálogo</button>
    </div>
  </div>
</section>

<!-- CONTACTO -->
<section class="contact" id="contacto">
  <div class="contact-wrap">
    <div>
      <div class="section-tag">Contacto</div>
      <h2 class="section-title">Hablemos de<br>su proyecto</h2>
      <div class="divider"></div>
      <div class="contact-item">
        <div class="contact-ico">✉</div>
        <div>
          <div class="contact-lbl">Email</div>
          <div class="contact-val">contacto@chileseating.cl</div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-ico">☎</div>
        <div>
          <div class="contact-lbl">Teléfono</div>
          <div class="contact-val">+56 2 2XXX XXXX</div>
        </div>
      </div>
      <div class="showrooms">
        <div class="showrooms-title">Nuestros Showrooms</div>
        <div class="showroom">
          <div class="showroom-name">Showroom Aeropuerto</div>
          <div class="showroom-addr">A pasos del Aeropuerto Internacional Arturo Merino Benítez</div>
        </div>
        <div class="showroom">
          <div class="showroom-name">Showroom Los Dominicos</div>
          <div class="showroom-addr">Metro Los Dominicos, Santiago</div>
        </div>
      </div>
    </div>
    <div>
      <form class="contact-form" id="contactForm" onsubmit="handleSubmit(event)">
        <div class="form-row">
          <div class="form-group">
            <label class="form-label">Nombre</label>
            <input class="form-input" type="text" placeholder="Juan Pérez" id="f-name">
          </div>
          <div class="form-group">
            <label class="form-label">Empresa</label>
            <input class="form-input" type="text" placeholder="Constructora XYZ" id="f-company">
          </div>
        </div>
        <div class="form-group">
          <label class="form-label">Email</label>
          <input class="form-input" type="email" placeholder="juan@empresa.cl" id="f-email">
        </div>
        <div class="form-group">
          <label class="form-label">Tipo de Recinto</label>
          <select class="form-select" id="f-type">
            <option value="">Seleccione...</option>
            <option>Teatro</option>
            <option>Auditorio</option>
            <option>Centro Cultural</option>
            <option>Estadio / Centro Deportivo</option>
            <option>Universidad / Colegio</option>
            <option>Otro</option>
          </select>
        </div>
        <div class="form-group">
          <label class="form-label">Cantidad aproximada de butacas</label>
          <input class="form-input" type="number" placeholder="Ej: 500" id="f-qty">
        </div>
        <div class="form-group">
          <label class="form-label">Mensaje</label>
          <textarea class="form-textarea" placeholder="Cuéntenos sobre su proyecto..." id="f-msg"></textarea>
        </div>
        <button type="submit" class="form-submit">Enviar Consulta →</button>
      </form>
      <div class="success-box" id="successBox">
        <h4>✓ Consulta enviada exitosamente</h4>
        <p>Nos comunicaremos con usted a la brevedad.</p>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>© 2025 ChileSeating · Todos los derechos reservados · <a href="https://www.chileseating.cl" target="_blank">www.chileseating.cl</a></p>
  <p>El mayor instalador de butacas en Chile · Teatros · Auditorios · Estadios · Centros Culturales</p>
</footer>

<script>
const projects=[
  {name:"Teatro Chiflón del Diablo",tag:"teatro",city:"Lota, Biobío",units:"813 butacas",bg:"#2A1510",accent:"#C9A84C",emoji:"🏛"},
  {name:"Teatro del Lago",tag:"teatro",city:"Panguipulli, Los Ríos",units:"Modelo París",bg:"#0A1628",accent:"#5BA3C5",emoji:"🎭"},
  {name:"Teatro Municipal Iquique",tag:"teatro",city:"Iquique, Tarapacá",units:"Modelo Resende",bg:"#1A1208",accent:"#E6B84A",emoji:"🎪"},
  {name:"Universidad de Concepción",tag:"universidad",city:"Concepción",units:"188 butacas Granada",bg:"#0F1E10",accent:"#5CB85C",emoji:"🎓"},
  {name:"Universidad del Bío-Bío",tag:"universidad",city:"Chillán",units:"274 butacas",bg:"#0D1420",accent:"#6496CE",emoji:"📚"},
  {name:"Colegio San Carlos de Apoquindo",tag:"universidad",city:"Las Condes, Santiago",units:"360 butacas",bg:"#1A0B16",accent:"#C07ABE",emoji:"🏫"},
  {name:"Chimkowe",tag:"cultural",city:"Peñalolén, Santiago",units:"Butacas + Alfombras",bg:"#0A1A12",accent:"#48B07E",emoji:"🎨"},
  {name:"Centro Cultural Renaico",tag:"cultural",city:"Renaico, Araucanía",units:"Modelo Minor Tandem",bg:"#1C1208",accent:"#D4884A",emoji:"🏗"},
  {name:"Aula Magna Coyhaique",tag:"estadio",city:"Coyhaique, Aysén",units:"Butacas Energy",bg:"#0C1018",accent:"#8AA0B2",emoji:"🏟"},
];

function renderProjects(filter){
  const g=document.getElementById('projGrid');
  const data=filter==='all'?projects:projects.filter(p=>p.tag===filter);
  g.innerHTML=data.map(p=>`
    <div class="proj-card" style="background:${p.bg}">
      <div class="proj-inner">
        <div class="proj-emoji">${p.emoji}</div>
        <div class="proj-units" style="color:${p.accent}">${p.units}</div>
      </div>
      <div class="proj-overlay">
        <div>
          <div class="proj-tag">${p.city}</div>
          <div class="proj-name">${p.name}</div>
          <div class="proj-detail">${p.tag.charAt(0).toUpperCase()+p.tag.slice(1)}</div>
        </div>
      </div>
      <div class="proj-footer">
        <div class="proj-footer-tag" style="color:${p.accent}">${p.city}</div>
        <div class="proj-footer-name">${p.name}</div>
      </div>
    </div>
  `).join('');
}

function filterProj(cat,btn){
  document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  renderProjects(cat);
}

function handleSubmit(e){
  e.preventDefault();
  const name=document.getElementById('f-name').value;
  const type=document.getElementById('f-type').value;
  if(!name||!type){alert('Por favor complete su nombre y el tipo de recinto.');return;}
  document.getElementById('contactForm').style.display='none';
  document.getElementById('successBox').style.display='block';
}

renderProjects('all');
</script>
</body>
</html>
