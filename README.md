<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>PetAmor — Os Melhores Produtos para o Seu Pet</title>
<meta name="description" content="Encontre os melhores produtos para cães e gatos com os menores preços na Amazon. Rações, brinquedos, higiene e muito mais!"/>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,400;0,700;0,900;1,400&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet"/>
<style>
:root {
  --cream: #fdf6ee;
  --warm: #f5ebe0;
  --brown: #6b4c3b;
  --brown-light: #a07060;
  --orange: #e8622a;
  --orange-light: #f08050;
  --green: #3a7d44;
  --green-light: #52a85f;
  --text: #2a1f1a;
  --muted: #8a7060;
  --white: #ffffff;
  --shadow: 0 8px 32px rgba(107,76,59,0.12);
  --shadow-lg: 0 20px 60px rgba(107,76,59,0.18);
}

* { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background: var(--cream);
  color: var(--text);
  font-family: 'Plus Jakarta Sans', sans-serif;
  overflow-x: hidden;
}

/* NOISE TEXTURE */
body::after {
  content: '';
  position: fixed; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  pointer-events: none; z-index: 9999; opacity: 1;
}

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  background: rgba(253,246,238,0.92);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(107,76,59,0.1);
  padding: 0 40px;
  display: flex; align-items: center; justify-content: space-between;
  height: 70px;
}
.nav-logo {
  font-family: 'Fraunces', serif;
  font-size: 26px; font-weight: 900;
  color: var(--orange);
  letter-spacing: -1px;
}
.nav-logo span { color: var(--brown); }
.nav-links { display: flex; gap: 32px; align-items: center; }
.nav-links a {
  text-decoration: none; color: var(--muted);
  font-size: 14px; font-weight: 600;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--orange); }
.nav-cta {
  background: var(--orange); color: #fff !important;
  padding: 10px 22px; border-radius: 50px;
  font-weight: 700 !important; font-size: 13px !important;
  transition: background 0.2s, transform 0.2s !important;
}
.nav-cta:hover { background: var(--orange-light) !important; transform: translateY(-1px); }

/* HERO */
.hero {
  min-height: 100vh;
  display: flex; align-items: center;
  padding: 120px 40px 80px;
  position: relative;
  overflow: hidden;
}
.hero-bg {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse 80% 80% at 70% 50%, rgba(232,98,42,0.08) 0%, transparent 70%),
              radial-gradient(ellipse 60% 60% at 20% 80%, rgba(58,125,68,0.06) 0%, transparent 60%);
}
.hero-paws {
  position: absolute; font-size: 120px; opacity: 0.04;
  animation: float 8s ease-in-out infinite;
}
.hero-paws:nth-child(1) { top: 10%; right: 5%; animation-delay: 0s; }
.hero-paws:nth-child(2) { bottom: 15%; right: 20%; font-size: 80px; animation-delay: 3s; }
.hero-paws:nth-child(3) { top: 40%; left: 2%; font-size: 60px; animation-delay: 5s; }
@keyframes float { 0%,100%{transform:translateY(0) rotate(0deg)} 50%{transform:translateY(-20px) rotate(5deg)} }

.hero-content { position: relative; z-index: 1; max-width: 640px; }
.hero-tag {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(232,98,42,0.1); color: var(--orange);
  padding: 8px 16px; border-radius: 50px;
  font-size: 13px; font-weight: 700;
  margin-bottom: 28px;
  animation: fadeUp 0.6s ease both;
}
.hero-tag-dot { width: 8px; height: 8px; background: var(--orange); border-radius: 50%; animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.4} }

.hero h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(48px, 7vw, 80px);
  font-weight: 900; line-height: 1.0;
  letter-spacing: -2px;
  animation: fadeUp 0.6s 0.1s ease both;
}
.hero h1 em { font-style: italic; color: var(--orange); }
.hero p {
  font-size: 18px; color: var(--muted); line-height: 1.7;
  margin: 24px 0 36px;
  animation: fadeUp 0.6s 0.2s ease both;
}
.hero-btns {
  display: flex; gap: 16px; flex-wrap: wrap;
  animation: fadeUp 0.6s 0.3s ease both;
}
.btn-main {
  background: var(--orange); color: #fff;
  padding: 16px 32px; border-radius: 50px;
  font-weight: 700; font-size: 15px;
  text-decoration: none; transition: all 0.2s;
  box-shadow: 0 8px 24px rgba(232,98,42,0.35);
}
.btn-main:hover { background: var(--orange-light); transform: translateY(-2px); box-shadow: 0 12px 32px rgba(232,98,42,0.45); }
.btn-secondary {
  background: transparent; color: var(--brown);
  padding: 16px 32px; border-radius: 50px;
  font-weight: 700; font-size: 15px;
  text-decoration: none; border: 2px solid rgba(107,76,59,0.2);
  transition: all 0.2s;
}
.btn-secondary:hover { border-color: var(--brown); background: rgba(107,76,59,0.05); }

.hero-stats {
  display: flex; gap: 40px; margin-top: 48px;
  animation: fadeUp 0.6s 0.4s ease both;
}
.stat-item {}
.stat-num { font-family: 'Fraunces', serif; font-size: 32px; font-weight: 900; color: var(--brown); }
.stat-label { font-size: 13px; color: var(--muted); margin-top: 2px; }

@keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }

/* CATEGORIES */
.categories { padding: 80px 40px; }
.section-header { text-align: center; margin-bottom: 48px; }
.section-tag {
  display: inline-block; background: rgba(58,125,68,0.1);
  color: var(--green); padding: 6px 16px; border-radius: 50px;
  font-size: 12px; font-weight: 700; text-transform: uppercase; letter-spacing: 1px;
  margin-bottom: 16px;
}
.section-title {
  font-family: 'Fraunces', serif;
  font-size: clamp(32px, 4vw, 48px);
  font-weight: 900; letter-spacing: -1px; line-height: 1.1;
}
.section-sub { color: var(--muted); font-size: 16px; margin-top: 12px; }

.cat-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; max-width: 1200px; margin: 0 auto; }
.cat-card {
  background: var(--white); border-radius: 20px;
  padding: 32px 24px; text-align: center;
  cursor: pointer; transition: all 0.3s;
  border: 2px solid transparent;
  text-decoration: none; color: var(--text);
  box-shadow: var(--shadow);
}
.cat-card:hover { transform: translateY(-6px); border-color: var(--orange); box-shadow: var(--shadow-lg); }
.cat-emoji { font-size: 48px; display: block; margin-bottom: 16px; }
.cat-name { font-family: 'Fraunces', serif; font-size: 20px; font-weight: 700; }
.cat-count { font-size: 13px; color: var(--muted); margin-top: 6px; }

/* PRODUCTS */
.products { padding: 80px 40px; background: var(--warm); }
.prod-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; max-width: 1200px; margin: 48px auto 0; }

.prod-card {
  background: var(--white); border-radius: 24px;
  overflow: hidden; transition: all 0.3s;
  box-shadow: var(--shadow);
}
.prod-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-lg); }

.prod-img {
  height: 200px; display: flex; align-items: center; justify-content: center;
  font-size: 80px; position: relative;
}
.prod-img.bg1 { background: linear-gradient(135deg, #fff5ee, #ffe4d0); }
.prod-img.bg2 { background: linear-gradient(135deg, #eef5ff, #d0e8ff); }
.prod-img.bg3 { background: linear-gradient(135deg, #eefff2, #d0f0d8); }
.prod-img.bg4 { background: linear-gradient(135deg, #fff8ee, #ffe8b0); }
.prod-img.bg5 { background: linear-gradient(135deg, #ffeef5, #ffd0e8); }
.prod-img.bg6 { background: linear-gradient(135deg, #f0eeff, #ddd0ff); }

.prod-badge {
  position: absolute; top: 14px; left: 14px;
  background: var(--orange); color: #fff;
  padding: 4px 12px; border-radius: 50px;
  font-size: 11px; font-weight: 700;
}
.prod-badge.green { background: var(--green); }

.prod-body { padding: 20px; }
.prod-cat { font-size: 11px; color: var(--muted); font-weight: 700; text-transform: uppercase; letter-spacing: 1px; }
.prod-name { font-family: 'Fraunces', serif; font-size: 18px; font-weight: 700; margin: 6px 0; line-height: 1.3; }
.prod-desc { font-size: 13px; color: var(--muted); line-height: 1.6; }
.prod-stars { color: #f4a400; font-size: 13px; margin: 10px 0 4px; }
.prod-reviews { font-size: 12px; color: var(--muted); }

.prod-footer {
  padding: 16px 20px; border-top: 1px solid rgba(107,76,59,0.08);
  display: flex; align-items: center; justify-content: space-between;
}
.prod-price { font-family: 'Fraunces', serif; font-size: 22px; font-weight: 900; color: var(--brown); }
.prod-price-old { font-size: 13px; color: var(--muted); text-decoration: line-through; }
.prod-btn {
  background: var(--orange); color: #fff;
  padding: 10px 20px; border-radius: 50px;
  font-size: 13px; font-weight: 700;
  text-decoration: none; transition: all 0.2s;
  white-space: nowrap;
}
.prod-btn:hover { background: var(--orange-light); transform: scale(1.05); }

/* DESTAQUES */
.highlight {
  padding: 80px 40px;
  display: flex; align-items: center; gap: 80px;
  max-width: 1200px; margin: 0 auto;
}
.highlight-text { flex: 1; }
.highlight-visual {
  flex: 1; display: flex; flex-direction: column; gap: 16px;
}
.highlight-card {
  background: var(--white); border-radius: 16px; padding: 20px 24px;
  display: flex; align-items: center; gap: 16px;
  box-shadow: var(--shadow); transition: transform 0.2s;
}
.highlight-card:hover { transform: translateX(8px); }
.hcard-emoji { font-size: 36px; flex-shrink: 0; }
.hcard-title { font-weight: 700; font-size: 15px; }
.hcard-sub { font-size: 13px; color: var(--muted); margin-top: 2px; }
.hcard-price { margin-left: auto; font-family: 'Fraunces', serif; font-size: 20px; font-weight: 900; color: var(--orange); flex-shrink: 0; }

/* NEWSLETTER */
.newsletter {
  background: var(--brown); color: var(--white);
  padding: 80px 40px; text-align: center;
  position: relative; overflow: hidden;
}
.newsletter::before {
  content: '🐾';
  position: absolute; font-size: 300px; opacity: 0.04;
  top: 50%; left: 50%; transform: translate(-50%,-50%);
}
.newsletter h2 {
  font-family: 'Fraunces', serif;
  font-size: clamp(28px, 4vw, 44px);
  font-weight: 900; margin-bottom: 16px; position: relative;
}
.newsletter p { color: rgba(255,255,255,0.7); font-size: 16px; margin-bottom: 36px; position: relative; }
.newsletter-form { display: flex; gap: 12px; max-width: 480px; margin: 0 auto; position: relative; }
.newsletter-form input {
  flex: 1; padding: 16px 24px; border-radius: 50px;
  border: none; font-size: 14px; font-family: 'Plus Jakarta Sans', sans-serif;
  outline: none; background: rgba(255,255,255,0.12); color: #fff;
}
.newsletter-form input::placeholder { color: rgba(255,255,255,0.5); }
.newsletter-form button {
  background: var(--orange); color: #fff;
  padding: 16px 28px; border-radius: 50px; border: none;
  font-weight: 700; font-size: 14px; cursor: pointer;
  font-family: 'Plus Jakarta Sans', sans-serif;
  transition: all 0.2s; white-space: nowrap;
}
.newsletter-form button:hover { background: var(--orange-light); transform: scale(1.05); }

/* FOOTER */
footer {
  background: var(--text); color: rgba(255,255,255,0.6);
  padding: 48px 40px 32px;
}
.footer-top {
  display: flex; justify-content: space-between; align-items: flex-start;
  gap: 40px; margin-bottom: 40px; flex-wrap: wrap;
}
.footer-brand .nav-logo { color: var(--orange); margin-bottom: 12px; display: block; }
.footer-brand p { font-size: 14px; max-width: 280px; line-height: 1.6; }
.footer-links h4 { color: #fff; font-size: 14px; font-weight: 700; margin-bottom: 16px; }
.footer-links a { display: block; color: rgba(255,255,255,0.5); text-decoration: none; font-size: 14px; margin-bottom: 10px; transition: color 0.2s; }
.footer-links a:hover { color: var(--orange); }
.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.08); padding-top: 24px;
  display: flex; justify-content: space-between; align-items: center;
  font-size: 13px; flex-wrap: wrap; gap: 12px;
}
.footer-disclaimer { font-size: 12px; color: rgba(255,255,255,0.3); margin-top: 12px; }

/* BACK TO TOP */
.back-top {
  position: fixed; bottom: 32px; right: 32px;
  background: var(--orange); color: #fff;
  width: 48px; height: 48px; border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 20px; cursor: pointer; z-index: 50;
  box-shadow: 0 4px 20px rgba(232,98,42,0.4);
  transition: all 0.2s; text-decoration: none;
  opacity: 0; transform: translateY(20px);
  transition: opacity 0.3s, transform 0.3s;
}
.back-top.visible { opacity: 1; transform: translateY(0); }
.back-top:hover { transform: translateY(-4px) !important; }

/* RESPONSIVE */
@media (max-width: 768px) {
  nav { padding: 0 20px; }
  .nav-links { display: none; }
  .hero { padding: 100px 20px 60px; }
  .hero-stats { gap: 24px; }
  .categories, .products, .newsletter { padding: 60px 20px; }
  .cat-grid { grid-template-columns: repeat(2, 1fr); }
  .prod-grid { grid-template-columns: 1fr; }
  .highlight { flex-direction: column; padding: 60px 20px; gap: 40px; }
  footer { padding: 40px 20px 24px; }
  .footer-top { flex-direction: column; }
  .newsletter-form { flex-direction: column; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Pet<span>Amor</span></div>
  <div class="nav-links">
    <a href="#categorias">Categorias</a>
    <a href="#produtos">Produtos</a>
    <a href="#destaques">Destaques</a>
    <a href="#newsletter" class="nav-cta">Receber Ofertas</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <span class="hero-paws">🐾</span>
  <span class="hero-paws">🐾</span>
  <span class="hero-paws">🐾</span>

  <div class="hero-content">
    <div class="hero-tag">
      <span class="hero-tag-dot"></span>
      Afiliado Amazon — Melhores preços garantidos
    </div>
    <h1>Tudo que seu<br/><em>Pet merece</em><br/>está aqui 🐶</h1>
    <p>Curadoria dos melhores produtos para cães e gatos na Amazon Brasil. Ração, higiene, brinquedos e muito mais com frete grátis Prime!</p>
    <div class="hero-btns">
      <a href="#produtos" class="btn-main">Ver Produtos ↓</a>
      <a href="#categorias" class="btn-secondary">Explorar Categorias</a>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">50+</div>
        <div class="stat-label">Produtos selecionados</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">4.8★</div>
        <div class="stat-label">Avaliação média</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">🚀</div>
        <div class="stat-label">Frete Prime grátis</div>
      </div>
    </div>
  </div>
</section>

<!-- CATEGORIAS -->
<section class="categories" id="categorias">
  <div class="section-header">
    <div class="section-tag">Categorias</div>
    <div class="section-title">O que seu pet<br/>precisa hoje?</div>
    <div class="section-sub">Selecione a categoria e encontre os melhores produtos</div>
  </div>
  <div class="cat-grid">
    <a href="#produtos" class="cat-card">
      <span class="cat-emoji">🍖</span>
      <div class="cat-name">Ração & Petiscos</div>
      <div class="cat-count">12 produtos</div>
    </a>
    <a href="#produtos" class="cat-card">
      <span class="cat-emoji">🛁</span>
      <div class="cat-name">Banho & Higiene</div>
      <div class="cat-count">8 produtos</div>
    </a>
    <a href="#produtos" class="cat-card">
      <span class="cat-emoji">🎾</span>
      <div class="cat-name">Brinquedos</div>
      <div class="cat-count">10 produtos</div>
    </a>
    <a href="#produtos" class="cat-card">
      <span class="cat-emoji">💊</span>
      <div class="cat-name">Saúde & Vitaminas</div>
      <div class="cat-count">9 produtos</div>
    </a>
  </div>
</section>

<!-- PRODUTOS -->
<section class="products" id="produtos">
  <div class="section-header">
    <div class="section-tag">Em Alta</div>
    <div class="section-title">Produtos mais<br/>recomendados</div>
    <div class="section-sub">Selecionados por custo-benefício e avaliações reais</div>
  </div>
  <div class="prod-grid">

    <!-- Produto 1 -->
    <div class="prod-card">
      <div class="prod-img bg1">
        🐕
        <div class="prod-badge">Mais Vendido</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🍖 Ração</div>
        <div class="prod-name">Ração Golden Retriever Premium 15kg</div>
        <div class="prod-desc">Fórmula completa com vitaminas e minerais para raças grandes. Sem corantes artificiais.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.8 · 2.341 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 219,90</div>
          <div class="prod-price">R$ 189,90</div>
        </div>
        <a href="https://amzn.to/4siAWVZ" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 2 -->
    <div class="prod-card">
      <div class="prod-img bg2">
        🐱
        <div class="prod-badge green">Prime</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🍖 Ração Gatos</div>
        <div class="prod-name">Whiskas Adulto Frango 10,1kg</div>
        <div class="prod-desc">Nutrição completa e balanceada para gatos adultos. Fórmula com taurina para saúde cardíaca.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.7 · 5.821 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 149,90</div>
          <div class="prod-price">R$ 129,90</div>
        </div>
        <a href="https://amzn.to/4cURizo" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 3 -->
    <div class="prod-card">
      <div class="prod-img bg3">
        🛁
        <div class="prod-badge">Oferta</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🛁 Higiene</div>
        <div class="prod-name">Kit Banho e Tosa Completo Pet</div>
        <div class="prod-desc">Shampoo, condicionador, escova e tesoura. Tudo que você precisa para cuidar em casa.</div>
        <div class="prod-stars">★★★★☆</div>
        <div class="prod-reviews">4.5 · 1.203 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 99,90</div>
          <div class="prod-price">R$ 79,90</div>
        </div>
        <a href="https://amzn.to/4cQ8cPx" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 4 -->
    <div class="prod-card">
      <div class="prod-img bg4">
        🎾
        <div class="prod-badge green">Prime</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🎾 Brinquedo</div>
        <div class="prod-name">Kit 5 Brinquedos Interativos Cães</div>
        <div class="prod-desc">Brinquedos de borracha resistente para estimular o seu cão. Ideal para raças ativas.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.9 · 876 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 69,90</div>
          <div class="prod-price">R$ 49,90</div>
        </div>
        <a href="https://amzn.to/4uUgeh1" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 5 -->
    <div class="prod-card">
      <div class="prod-img bg5">
        💊
        <div class="prod-badge">Saúde</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">💊 Vitaminas</div>
        <div class="prod-name">Suplemento Condroitina + Glucosamina Cães</div>
        <div class="prod-desc">Protege as articulações de cães idosos e de raças grandes. 60 comprimidos palatáveis.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.8 · 3.102 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 89,90</div>
          <div class="prod-price">R$ 69,90</div>
        </div>
        <a href="https://amzn.to/3PKgeQf" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 6 -->
    <div class="prod-card">
      <div class="prod-img bg6">
        🏠
        <div class="prod-badge green">Prime</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🏠 Acessórios</div>
        <div class="prod-name">Cama Pet Luxo Lavável Antialérgica</div>
        <div class="prod-desc">Tecido macio antialérgico com enchimento premium. Disponível em 3 tamanhos. Lavável na máquina.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.9 · 2.567 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 159,90</div>
          <div class="prod-price">R$ 119,90</div>
        </div>
        <a href="https://amzn.to/47RgvXM" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

    <!-- Produto 7 -->
    <div class="prod-card">
      <div class="prod-img bg1">
        🦴
        <div class="prod-badge green">Novo</div>
      </div>
      <div class="prod-body">
        <div class="prod-cat">🎾 Petisco</div>
        <div class="prod-name">Petisco Natural para Cães e Gatos</div>
        <div class="prod-desc">Snack saudável e saboroso. Sem conservantes artificiais. Ideal para treino e recompensa.</div>
        <div class="prod-stars">★★★★★</div>
        <div class="prod-reviews">4.7 · 1.450 avaliações</div>
      </div>
      <div class="prod-footer">
        <div>
          <div class="prod-price-old">R$ 59,90</div>
          <div class="prod-price">R$ 44,90</div>
        </div>
        <a href="https://amzn.to/4sQZy80" target="_blank" class="prod-btn">Ver na Amazon →</a>
      </div>
    </div>

  </div>

  <!-- BOTÕES VER TODOS -->
  <div style="text-align:center;margin-top:48px;display:flex;gap:16px;justify-content:center;flex-wrap:wrap;">
    <a href="https://www.amazon.com.br/s?k=pets+c%C3%A3es+todos+produtos&__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3G2T89ZVCHC50&sprefix=pets+c%C3%A3es+todos+produtos%2Caps%2C254&linkCode=ll2&tag=joaquim013-20&linkId=5a3ddc5111978832b9e660a0b2569615&ref_=as_li_ss_tl" target="_blank"
      style="background:var(--orange);color:#fff;padding:16px 36px;border-radius:50px;font-weight:700;font-size:15px;text-decoration:none;box-shadow:0 8px 24px rgba(232,98,42,0.35);transition:all 0.2s;display:inline-block;"
      onmouseover="this.style.transform='translateY(-2px)'" onmouseout="this.style.transform='translateY(0)'">
      🐾 Ver Todos os Produtos Pet
    </a>
    <a href="https://www.amazon.com.br/s?k=pets+caes&__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=R3L3VR3O0O6X&sprefix=pets+caes%2Caps%2C255&linkCode=ll2&tag=joaquim013-20&linkId=c8acbd1f99c5d44c435edf4a8a5dd020&ref_=as_li_ss_tl" target="_blank"
      style="background:var(--green);color:#fff;padding:16px 36px;border-radius:50px;font-weight:700;font-size:15px;text-decoration:none;box-shadow:0 8px 24px rgba(58,125,68,0.3);transition:all 0.2s;display:inline-block;"
      onmouseover="this.style.transform='translateY(-2px)'" onmouseout="this.style.transform='translateY(0)'">
      🐶 Ver Produtos para Cães
    </a>
  </div>

</section>

<!-- DESTAQUES -->
<section id="destaques">
  <div class="highlight">
    <div class="highlight-text">
      <div class="section-tag">Por que comprar aqui?</div>
      <div class="section-title" style="text-align:left;margin-top:16px">Só indico o que<br/><em style="font-style:italic;color:var(--orange)">realmente vale</em></div>
      <p style="color:var(--muted);margin-top:20px;font-size:16px;line-height:1.7">Todos os produtos são testados e avaliados antes de serem recomendados. Meu compromisso é com a saúde e felicidade do seu pet — não com qualquer produto patrocinado.</p>
      <div style="margin-top:32px;display:flex;flex-direction:column;gap:16px">
        <div style="display:flex;align-items:center;gap:12px">
          <span style="font-size:24px">✅</span>
          <span style="font-size:15px;color:var(--muted)">Preços conferidos diariamente na Amazon</span>
        </div>
        <div style="display:flex;align-items:center;gap:12px">
          <span style="font-size:24px">✅</span>
          <span style="font-size:15px;color:var(--muted)">Só produtos com mais de 4.5 estrelas</span>
        </div>
        <div style="display:flex;align-items:center;gap:12px">
          <span style="font-size:24px">✅</span>
          <span style="font-size:15px;color:var(--muted)">Frete Prime grátis em todos os itens</span>
        </div>
      </div>
    </div>
    <div class="highlight-visual">
      <div class="highlight-card">
        <span class="hcard-emoji">🐶</span>
        <div>
          <div class="hcard-title">Ração Premium Cães</div>
          <div class="hcard-sub">⭐ 4.8 · Mais vendido</div>
        </div>
        <div class="hcard-price">R$189</div>
      </div>
      <div class="highlight-card">
        <span class="hcard-emoji">🐱</span>
        <div>
          <div class="hcard-title">Ração Gatos Adultos</div>
          <div class="hcard-sub">⭐ 4.7 · Prime grátis</div>
        </div>
        <div class="hcard-price">R$129</div>
      </div>
      <div class="highlight-card">
        <span class="hcard-emoji">💊</span>
        <div>
          <div class="hcard-title">Vitamina Articulações</div>
          <div class="hcard-sub">⭐ 4.8 · Oferta hoje</div>
        </div>
        <div class="hcard-price">R$69</div>
      </div>
      <div class="highlight-card">
        <span class="hcard-emoji">🛁</span>
        <div>
          <div class="hcard-title">Kit Banho Completo</div>
          <div class="hcard-sub">⭐ 4.5 · Frete grátis</div>
        </div>
        <div class="hcard-price">R$79</div>
      </div>
    </div>
  </div>
</section>

<!-- NEWSLETTER -->
<section class="newsletter" id="newsletter">
  <h2>Receba ofertas exclusivas<br/>para pets toda semana 🐾</h2>
  <p>Cadastre seu WhatsApp ou e-mail e seja o primeiro a saber das promoções</p>
  <div class="newsletter-form">
    <input type="email" placeholder="seu@email.com ou WhatsApp"/>
    <button onclick="alert('Cadastrado! Você receberá as melhores ofertas 🐾')">Quero Ofertas!</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div class="footer-brand">
      <span class="nav-logo">Pet<span style="color:#fff">Amor</span></span>
      <p>Curadoria dos melhores produtos pet na Amazon Brasil. Seu pet merece o melhor!</p>
      <div style="margin-top:16px;display:flex;gap:12px">
        <a href="https://instagram.com/Jr4360494" target="_blank" style="color:var(--orange);font-size:13px;font-weight:700;text-decoration:none">📸 Instagram</a>
        <a href="https://wa.me/55" target="_blank" style="color:var(--orange);font-size:13px;font-weight:700;text-decoration:none">💬 WhatsApp</a>
      </div>
    </div>
    <div class="footer-links">
      <h4>Categorias</h4>
      <a href="#produtos">🍖 Ração & Petiscos</a>
      <a href="#produtos">🛁 Banho & Higiene</a>
      <a href="#produtos">🎾 Brinquedos</a>
      <a href="#produtos">💊 Saúde & Vitaminas</a>
    </div>
    <div class="footer-links">
      <h4>Links</h4>
      <a href="#categorias">Categorias</a>
      <a href="#produtos">Produtos</a>
      <a href="https://instagram.com/Jr4360494" target="_blank">Instagram</a>
      <a href="#newsletter">Receber Ofertas</a>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2026 PetAmor — Todos os direitos reservados</span>
    <span>Feito com ❤️ para pets e seus donos</span>
  </div>
  <div class="footer-disclaimer">
    ⚠️ Este site participa do Programa de Afiliados da Amazon. Ao clicar nos links e realizar uma compra, podemos receber uma comissão sem custo adicional para você.
  </div>
</footer>

<!-- BACK TO TOP -->
<a href="#" class="back-top" id="backTop">↑</a>

<script>
// Back to top
const backTop = document.getElementById('backTop');
window.addEventListener('scroll', () => {
  if (window.scrollY > 400) backTop.classList.add('visible');
  else backTop.classList.remove('visible');
});

// Animação ao scroll
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.style.opacity = '1';
      e.target.style.transform = 'translateY(0)';
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.prod-card, .cat-card, .highlight-card').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(30px)';
  el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
  observer.observe(el);
});
</script>
</body>
</html>
