[luxetrailholidays (3).html](https://github.com/user-attachments/files/28178849/luxetrailholidays.3.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>LuxeTrail Holidays – India's Premium Travel Community | Book Your Trip!</title>
<meta name="description" content="India's top luxury travel community for group trips, treks & custom tours. Trusted by 50,000+ travellers with expert guides & curated experiences."/>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;900&family=DM+Sans:wght@300;400;500;600&family=Bebas+Neue&display=swap" rel="stylesheet"/>
<style>
  :root {
    --primary: #e8521a;
    --primary-dark: #c43e0a;
    --secondary: #1a2744;
    --accent: #f5c842;
    --light-bg: #fdf9f5;
    --card-bg: #ffffff;
    --text: #1a1a1a;
    --text-muted: #6b7280;
    --border: #e5e7eb;
    --nav-h: 68px;
    --radius: 12px;
    --shadow: 0 4px 24px rgba(0,0,0,0.10);
    --shadow-lg: 0 8px 48px rgba(0,0,0,0.16);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { font-family: 'DM Sans', sans-serif; color: var(--text); background: #fff; overflow-x: hidden; }

  /* ─── NAVBAR ─── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    height: var(--nav-h);
    background: rgba(255,255,255,0.97);
    backdrop-filter: blur(12px);
    box-shadow: 0 1px 16px rgba(0,0,0,0.08);
    display: flex; align-items: center;
  }
  .nav-inner {
    max-width: 1280px; width: 100%; margin: 0 auto;
    padding: 0 24px;
    display: flex; align-items: center; justify-content: space-between; gap: 16px;
  }
  .logo {
    display: flex; align-items: center; gap: 10px; text-decoration: none;
    flex-shrink: 0;
  }
  .logo-icon {
    width: 40px; height: 40px; background: var(--primary);
    border-radius: 8px; display: flex; align-items: center; justify-content: center;
  }
  .logo-icon svg { width: 22px; height: 22px; fill: #fff; }
  .logo-text { font-family: 'Playfair Display', serif; font-size: 1.25rem; font-weight: 700; color: var(--secondary); line-height: 1.1; }
  .logo-text span { color: var(--primary); }
  .nav-links {
    display: flex; align-items: center; gap: 4px; list-style: none; flex: 1;
  }
  .nav-links > li { position: relative; }
  .nav-links > li > a {
    display: flex; align-items: center; gap: 4px;
    padding: 8px 12px; border-radius: 8px;
    text-decoration: none; font-size: 0.875rem; font-weight: 500; color: var(--secondary);
    transition: background 0.2s, color 0.2s;
    white-space: nowrap;
  }
  .nav-links > li > a:hover { background: #f3f4f6; color: var(--primary); }
  .nav-links > li > a .arrow { font-size: 0.65rem; opacity: 0.5; }
  .dropdown {
    display: none; position: absolute; top: calc(100% + 8px); left: 0;
    background: #fff; border-radius: 12px; box-shadow: var(--shadow-lg);
    padding: 8px; min-width: 200px; z-index: 999;
    border: 1px solid var(--border);
  }
  .nav-links > li:hover .dropdown { display: block; }
  .dropdown a {
    display: block; padding: 8px 14px; border-radius: 8px;
    text-decoration: none; font-size: 0.85rem; color: var(--text); font-weight: 400;
    transition: background 0.15s;
  }
  .dropdown a:hover { background: #fff5f0; color: var(--primary); }
  .nav-actions { display: flex; align-items: center; gap: 10px; flex-shrink: 0; }
  .nav-phone { font-size: 0.8rem; font-weight: 600; color: var(--secondary); text-decoration: none; }
  .btn-login {
    padding: 8px 20px; border-radius: 8px; border: 1.5px solid var(--primary);
    background: transparent; color: var(--primary); font-size: 0.85rem; font-weight: 600;
    cursor: pointer; transition: all 0.2s;
  }
  .btn-login:hover { background: var(--primary); color: #fff; }
  .btn-book {
    padding: 8px 20px; border-radius: 8px; border: none;
    background: var(--primary); color: #fff; font-size: 0.85rem; font-weight: 600;
    cursor: pointer; transition: all 0.2s;
  }
  .btn-book:hover { background: var(--primary-dark); transform: translateY(-1px); box-shadow: 0 4px 16px rgba(232,82,26,0.35); }

  /* ─── HERO ─── */
  .hero {
    height: 100vh; min-height: 600px;
    position: relative; overflow: hidden;
    display: flex; align-items: flex-end;
    padding-bottom: 80px;
  }
  .hero-slides { position: absolute; inset: 0; }
  .hero-slide {
    position: absolute; inset: 0;
    background-size: cover; background-position: center;
    opacity: 0; transition: opacity 1.2s ease;
  }
  .hero-slide.active { opacity: 1; }
  .hero-slide::after {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(15,20,40,0.85) 0%, rgba(15,20,40,0.25) 60%, transparent 100%);
  }
  .hero-slide:nth-child(1) { background-image: url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=1800&q=80'); }
  .hero-slide:nth-child(2) { background-image: url('https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=1800&q=80'); }
  .hero-slide:nth-child(3) { background-image: url('https://images.unsplash.com/photo-1433086966358-54859d0ed716?w=1800&q=80'); }
  .hero-slide:nth-child(4) { background-image: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=1800&q=80'); }
  .hero-slide:nth-child(5) { background-image: url('https://images.unsplash.com/photo-1501854140801-50d01698950b?w=1800&q=80'); }
  .hero-content {
    position: relative; z-index: 2;
    max-width: 1280px; width: 100%; margin: 0 auto; padding: 0 24px;
  }
  .hero-subtitle {
    font-size: 0.9rem; font-weight: 600; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 12px;
  }
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 7vw, 6rem); font-weight: 900;
    color: #fff; line-height: 1.0;
    margin-bottom: 8px;
  }
  .hero-places {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(2rem, 5vw, 4rem); color: var(--primary);
    height: 1.2em; overflow: hidden; line-height: 1.2;
    margin-bottom: 20px;
  }
  .hero-places-inner { transition: transform 0.7s cubic-bezier(0.4,0,0.2,1); }
  .hero-places-inner div { height: 1.2em; }
  .hero-tagline { font-size: 1rem; color: rgba(255,255,255,0.75); margin-bottom: 32px; font-style: italic; }
  .hero-cta { display: flex; gap: 14px; flex-wrap: wrap; }
  .cta-primary {
    padding: 14px 32px; border-radius: 10px; border: none;
    background: var(--primary); color: #fff; font-size: 1rem; font-weight: 600;
    cursor: pointer; transition: all 0.2s; text-decoration: none; display: inline-block;
  }
  .cta-primary:hover { background: var(--primary-dark); transform: translateY(-2px); box-shadow: 0 6px 24px rgba(232,82,26,0.45); }
  .cta-secondary {
    padding: 14px 32px; border-radius: 10px; border: 2px solid rgba(255,255,255,0.6);
    background: transparent; color: #fff; font-size: 1rem; font-weight: 600;
    cursor: pointer; transition: all 0.2s; text-decoration: none; display: inline-block;
  }
  .cta-secondary:hover { border-color: #fff; background: rgba(255,255,255,0.1); }
  .hero-dots {
    position: absolute; bottom: 32px; left: 50%; transform: translateX(-50%);
    z-index: 3; display: flex; gap: 8px;
  }
  .hero-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: rgba(255,255,255,0.4); cursor: pointer; transition: all 0.3s;
  }
  .hero-dot.active { background: var(--primary); width: 24px; border-radius: 4px; }

  /* ─── STATS STRIP ─── */
  .stats-strip {
    background: var(--secondary);
    padding: 28px 0;
  }
  .stats-inner {
    max-width: 1280px; margin: 0 auto; padding: 0 24px;
    display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px;
  }
  .stat-item { text-align: center; }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 700; color: var(--accent);
    display: block;
  }
  .stat-label { font-size: 0.82rem; color: rgba(255,255,255,0.65); margin-top: 4px; }

  /* ─── SECTION WRAPPER ─── */
  .section { padding: 64px 0; }
  .section-alt { background: var(--light-bg); }
  .section-inner { max-width: 1280px; margin: 0 auto; padding: 0 24px; }
  .section-header { margin-bottom: 36px; }
  .section-eyebrow {
    font-size: 0.75rem; font-weight: 700; letter-spacing: 0.18em;
    text-transform: uppercase; color: var(--primary); margin-bottom: 8px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 700; color: var(--secondary);
  }

  /* ─── CATEGORY PILLS ─── */
  .tabs { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 28px; }
  .tab {
    padding: 8px 18px; border-radius: 50px;
    border: 1.5px solid var(--border);
    background: #fff; font-size: 0.85rem; font-weight: 500; color: var(--text-muted);
    cursor: pointer; transition: all 0.2s;
  }
  .tab.active, .tab:hover { background: var(--primary); color: #fff; border-color: var(--primary); }

  /* ─── TRIP CARDS ─── */
  .cards-grid {
    display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 24px;
  }
  .trip-card {
    border-radius: var(--radius); overflow: hidden;
    background: var(--card-bg); box-shadow: var(--shadow);
    transition: transform 0.25s, box-shadow 0.25s;
    cursor: pointer; text-decoration: none; color: inherit; display: block;
  }
  .trip-card:hover { transform: translateY(-6px); box-shadow: var(--shadow-lg); }
  .card-img {
    width: 100%; height: 200px; object-fit: cover; display: block;
    background: #e5e7eb;
    position: relative;
  }
  .card-img-wrap { position: relative; overflow: hidden; height: 200px; }
  .card-img-wrap img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s; }
  .trip-card:hover .card-img-wrap img { transform: scale(1.05); }
  .card-badge {
    position: absolute; top: 12px; left: 12px;
    background: var(--accent); color: var(--secondary);
    font-size: 0.7rem; font-weight: 700; padding: 4px 10px; border-radius: 50px;
  }
  .card-body { padding: 16px; }
  .card-title { font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; line-height: 1.4; color: var(--secondary); }
  .card-meta { font-size: 0.78rem; color: var(--text-muted); display: flex; flex-wrap: wrap; gap: 6px; align-items: center; margin-bottom: 12px; }
  .card-dot { width: 3px; height: 3px; background: var(--text-muted); border-radius: 50%; }
  .card-price { display: flex; align-items: baseline; gap: 8px; }
  .card-price-current { font-family: 'Playfair Display', serif; font-size: 1.2rem; font-weight: 700; color: var(--primary); }
  .card-price-old { font-size: 0.8rem; text-decoration: line-through; color: var(--text-muted); }
  .card-price-discount { font-size: 0.75rem; font-weight: 600; color: #16a34a; background: #dcfce7; padding: 2px 8px; border-radius: 50px; }

  /* ─── CATEGORY ICONS ─── */
  .category-grid {
    display: grid; grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    gap: 16px;
  }
  .category-item {
    display: flex; flex-direction: column; align-items: center; gap: 10px;
    padding: 20px 12px; border-radius: var(--radius);
    background: #fff; border: 1.5px solid var(--border);
    cursor: pointer; text-decoration: none; color: inherit;
    transition: all 0.2s; text-align: center;
  }
  .category-item:hover { border-color: var(--primary); background: #fff5f0; transform: translateY(-3px); }
  .cat-icon {
    width: 52px; height: 52px; border-radius: 50%;
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    display: flex; align-items: center; justify-content: center;
    font-size: 1.4rem;
  }
  .cat-label { font-size: 0.78rem; font-weight: 600; color: var(--secondary); }

  /* ─── PROMOTIONAL BANNER ─── */
  .promo-banner {
    border-radius: var(--radius); overflow: hidden;
    height: 200px; position: relative; margin-bottom: 32px;
    background: linear-gradient(135deg, var(--secondary) 0%, #2d3e6e 100%);
    display: flex; align-items: center; padding: 32px;
  }
  .promo-banner h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem; color: #fff; max-width: 50%;
  }
  .promo-banner span { color: var(--accent); }
  .promo-btn {
    margin-left: auto;
    padding: 12px 28px; background: var(--primary); color: #fff;
    border-radius: 8px; font-weight: 600; text-decoration: none; font-size: 0.9rem;
    transition: all 0.2s;
  }
  .promo-btn:hover { background: var(--primary-dark); }

  /* ─── UPCOMING TRIPS TABLE ─── */
  .upcoming-grid { display: flex; flex-direction: column; gap: 12px; }
  .upcoming-item {
    display: grid; grid-template-columns: 80px 1fr auto auto;
    gap: 16px; align-items: center;
    background: #fff; border-radius: 10px;
    padding: 16px 20px; border: 1px solid var(--border);
    transition: box-shadow 0.2s; cursor: pointer; text-decoration: none; color: inherit;
  }
  .upcoming-item:hover { box-shadow: var(--shadow); }
  .upcoming-date { text-align: center; }
  .upcoming-date .day { font-family: 'Playfair Display', serif; font-size: 1.6rem; font-weight: 700; color: var(--primary); line-height: 1; }
  .upcoming-date .month { font-size: 0.72rem; font-weight: 600; color: var(--text-muted); text-transform: uppercase; }
  .upcoming-name { font-weight: 600; color: var(--secondary); font-size: 0.95rem; }
  .upcoming-dur { font-size: 0.78rem; color: var(--text-muted); margin-top: 2px; }
  .upcoming-seats { font-size: 0.8rem; font-weight: 600; color: #16a34a; white-space: nowrap; }
  .upcoming-price { font-family: 'Playfair Display', serif; font-size: 1.1rem; font-weight: 700; color: var(--primary); white-space: nowrap; }

  /* ─── REVIEWS ─── */
  .reviews-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 24px; }
  .review-card {
    background: #fff; border-radius: var(--radius); padding: 24px;
    border: 1px solid var(--border); box-shadow: var(--shadow);
    display: flex; flex-direction: column; gap: 16px;
  }
  .review-stars { color: var(--accent); font-size: 0.9rem; letter-spacing: 2px; }
  .review-text { font-size: 0.88rem; line-height: 1.7; color: var(--text-muted); flex: 1; }
  .review-author { display: flex; align-items: center; gap: 12px; }
  .review-avatar {
    width: 44px; height: 44px; border-radius: 50%;
    background: linear-gradient(135deg, var(--primary), var(--accent));
    display: flex; align-items: center; justify-content: center;
    font-weight: 700; font-size: 1rem; color: #fff; flex-shrink: 0;
  }
  .review-name { font-weight: 600; font-size: 0.9rem; color: var(--secondary); }
  .review-trip { font-size: 0.75rem; color: var(--text-muted); margin-top: 2px; }
  .review-img-trip { width: 100%; height: 130px; object-fit: cover; border-radius: 8px; }
  .try-link { font-size: 0.8rem; color: var(--primary); font-weight: 600; text-decoration: none; display: inline-flex; align-items: center; gap: 4px; }

  /* ─── WHY US ─── */
  .why-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 24px; }
  .why-card {
    text-align: center; padding: 32px 20px;
    border-radius: var(--radius); background: #fff;
    box-shadow: var(--shadow); border-bottom: 3px solid var(--primary);
  }
  .why-icon { font-size: 2.4rem; margin-bottom: 14px; }
  .why-title { font-weight: 700; font-size: 1rem; color: var(--secondary); margin-bottom: 8px; }
  .why-desc { font-size: 0.83rem; color: var(--text-muted); line-height: 1.6; }

  /* ─── ABOUT ─── */
  .about-wrap {
    display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: center;
  }
  .about-img-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .about-img-grid img { width: 100%; border-radius: 10px; object-fit: cover; }
  .about-img-grid img:first-child { grid-row: span 2; height: 320px; }
  .about-img-grid img:not(:first-child) { height: 150px; }
  .about-text p { font-size: 0.95rem; line-height: 1.8; color: var(--text-muted); margin-bottom: 16px; }
  .about-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 28px; }
  .about-stat-item { background: var(--light-bg); padding: 16px; border-radius: 10px; text-align: center; }
  .about-stat-num { font-family: 'Playfair Display', serif; font-size: 1.6rem; font-weight: 700; color: var(--primary); display: block; }
  .about-stat-label { font-size: 0.78rem; color: var(--text-muted); margin-top: 4px; }

  /* ─── FAQ ─── */
  .faq-list { max-width: 800px; }
  .faq-item {
    border: 1px solid var(--border); border-radius: 10px; margin-bottom: 10px;
    overflow: hidden;
  }
  .faq-q {
    width: 100%; text-align: left; background: #fff;
    padding: 18px 20px; font-size: 0.95rem; font-weight: 600; color: var(--secondary);
    border: none; cursor: pointer; display: flex; justify-content: space-between; align-items: center;
    transition: background 0.2s;
  }
  .faq-q:hover { background: #fff5f0; }
  .faq-q .faq-icon { font-size: 1.2rem; color: var(--primary); flex-shrink: 0; transition: transform 0.3s; }
  .faq-a { display: none; padding: 0 20px 18px; font-size: 0.88rem; line-height: 1.7; color: var(--text-muted); }
  .faq-item.open .faq-a { display: block; }
  .faq-item.open .faq-icon { transform: rotate(45deg); }

  /* ─── BLOGS ─── */
  .blog-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 24px; }
  .blog-card {
    border-radius: var(--radius); overflow: hidden;
    background: #fff; box-shadow: var(--shadow);
    text-decoration: none; color: inherit; display: block;
    transition: transform 0.25s;
  }
  .blog-card:hover { transform: translateY(-4px); }
  .blog-card img { width: 100%; height: 180px; object-fit: cover; }
  .blog-body { padding: 16px; }
  .blog-date { font-size: 0.72rem; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 8px; }
  .blog-title { font-weight: 600; font-size: 0.95rem; color: var(--secondary); line-height: 1.5; margin-bottom: 8px; }
  .blog-read { font-size: 0.78rem; color: var(--primary); font-weight: 600; }

  /* ─── RECOGNITIONS ─── */
  .recog-strip {
    display: flex; gap: 32px; flex-wrap: wrap; align-items: center; justify-content: center;
  }
  .recog-badge {
    background: #fff; border: 1.5px solid var(--border);
    border-radius: 10px; padding: 14px 24px;
    font-size: 0.8rem; font-weight: 700; color: var(--secondary);
    display: flex; align-items: center; gap: 8px;
  }
  .recog-badge span { font-size: 1.2rem; }

  /* ─── NEWSLETTER ─── */
  .newsletter {
    background: linear-gradient(135deg, var(--secondary) 0%, #1e3462 100%);
    border-radius: var(--radius);
    padding: 48px 40px;
    display: flex; gap: 40px; align-items: center; justify-content: space-between;
    flex-wrap: wrap;
  }
  .newsletter h2 {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; color: #fff;
  }
  .newsletter p { color: rgba(255,255,255,0.65); margin-top: 8px; font-size: 0.92rem; }
  .newsletter-form { display: flex; gap: 10px; flex-wrap: wrap; }
  .newsletter-form input {
    padding: 12px 20px; border-radius: 8px; border: none;
    font-size: 0.9rem; width: 280px; outline: none;
    font-family: 'DM Sans', sans-serif;
  }
  .newsletter-form button {
    padding: 12px 24px; border-radius: 8px; border: none;
    background: var(--primary); color: #fff; font-size: 0.9rem; font-weight: 600;
    cursor: pointer; transition: all 0.2s; font-family: 'DM Sans', sans-serif;
  }
  .newsletter-form button:hover { background: var(--primary-dark); }

  /* ─── FOOTER ─── */
  footer { background: var(--secondary); color: rgba(255,255,255,0.7); padding: 64px 0 0; }
  .footer-inner {
    max-width: 1280px; margin: 0 auto; padding: 0 24px;
    display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 40px;
  }
  .footer-brand .logo-text { color: #fff; }
  .footer-brand p { font-size: 0.85rem; line-height: 1.7; margin-top: 14px; }
  .footer-contact { font-size: 0.85rem; margin-top: 14px; }
  .footer-contact a { color: rgba(255,255,255,0.7); text-decoration: none; display: block; margin-bottom: 6px; }
  .footer-contact a:hover { color: var(--accent); }
  .footer-socials { display: flex; gap: 10px; margin-top: 16px; flex-wrap: wrap; }
  .social-btn {
    width: 36px; height: 36px; border-radius: 8px;
    background: rgba(255,255,255,0.1); display: flex; align-items: center; justify-content: center;
    text-decoration: none; font-size: 0.85rem; color: rgba(255,255,255,0.7);
    transition: all 0.2s;
  }
  .social-btn:hover { background: var(--primary); color: #fff; }
  .footer-col h4 { font-weight: 700; color: #fff; font-size: 0.9rem; margin-bottom: 16px; }
  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 8px; }
  .footer-col ul li a { font-size: 0.85rem; color: rgba(255,255,255,0.6); text-decoration: none; transition: color 0.2s; }
  .footer-col ul li a:hover { color: var(--accent); }
  .footer-bottom {
    margin-top: 48px; border-top: 1px solid rgba(255,255,255,0.1);
    padding: 20px 24px; display: flex; justify-content: space-between; align-items: center;
    max-width: 1280px; margin-left: auto; margin-right: auto; flex-wrap: wrap; gap: 10px;
  }
  .footer-bottom-copy { font-size: 0.8rem; }
  .footer-bottom-links { display: flex; gap: 16px; }
  .footer-bottom-links a { font-size: 0.8rem; color: rgba(255,255,255,0.5); text-decoration: none; }
  .footer-bottom-links a:hover { color: var(--accent); }

  /* ─── VIEW ALL BTN ─── */
  .view-all-wrap { text-align: center; margin-top: 32px; }
  .btn-view-all {
    display: inline-block; padding: 12px 36px; border-radius: 8px;
    border: 2px solid var(--primary); color: var(--primary);
    font-weight: 600; font-size: 0.9rem; text-decoration: none;
    transition: all 0.2s; background: transparent;
  }
  .btn-view-all:hover { background: var(--primary); color: #fff; }

  /* ─── HAMBURGER ─── */
  .ham { display: none; flex-direction: column; gap: 5px; cursor: pointer; background: none; border: none; padding: 4px; }
  .ham span { width: 24px; height: 2px; background: var(--secondary); border-radius: 2px; transition: all 0.3s; display: block; }
  .mobile-menu { display: none; position: fixed; inset: 0; top: var(--nav-h); background: #fff; z-index: 999; overflow-y: auto; padding: 20px 24px; flex-direction: column; gap: 4px; }
  .mobile-menu.open { display: flex; }
  .mobile-menu a { padding: 12px 16px; border-radius: 8px; text-decoration: none; font-size: 1rem; font-weight: 500; color: var(--secondary); border-bottom: 1px solid var(--border); }
  .mobile-menu a:hover { background: #fff5f0; color: var(--primary); }
  .mobile-menu .mm-section { font-weight: 700; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.12em; color: var(--primary); padding: 16px 0 4px; border-bottom: none; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .nav-phone { display: none; }
    .ham { display: flex; }
    .about-wrap { grid-template-columns: 1fr; }
    .footer-inner { grid-template-columns: 1fr 1fr; }
    .stats-inner { grid-template-columns: repeat(2, 1fr); }
  }
  @media (max-width: 600px) {
    .footer-inner { grid-template-columns: 1fr; }
    .upcoming-item { grid-template-columns: 60px 1fr auto; }
    .upcoming-price { display: none; }
    .newsletter { padding: 32px 24px; }
    .newsletter-form input { width: 100%; }
    .promo-banner h3 { font-size: 1.2rem; }
    .hero-title { font-size: 2.4rem; }
  }

  /* ─── ANIMATION ─── */
  @keyframes fadeUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
  .fade-up { animation: fadeUp 0.7s ease forwards; opacity: 0; }
  .fade-up-d1 { animation-delay: 0.1s; }
  .fade-up-d2 { animation-delay: 0.25s; }
  .fade-up-d3 { animation-delay: 0.4s; }
  .fade-up-d4 { animation-delay: 0.55s; }
</style>
</head>
<body>

<!-- ═══ NAVBAR ═══ -->
<nav>
  <div class="nav-inner">
    <a href="#" class="logo">
      <div class="logo-icon">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
      </div>
      <div class="logo-text"><span>LuxeTrail</span> Holidays</div>
    </a>

    <ul class="nav-links">
      <li>
        <a href="#trips">Backpacking <span class="arrow">▾</span></a>
        <div class="dropdown">
          <a href="#trips">Ladakh</a>
          <a href="#trips">Spiti Valley</a>
          <a href="#trips">Kashmir</a>
          <a href="#trips">Tawang</a>
          <a href="#trips">Meghalaya</a>
        </div>
      </li>
      <li>
        <a href="#bestsellers">Best Sellers <span class="arrow">▾</span></a>
        <div class="dropdown">
          <a href="#bestsellers">Spiti Bike Tour</a>
          <a href="#bestsellers">Bali with Gili Island</a>
          <a href="#bestsellers">Valley of Flowers Trek</a>
          <a href="#bestsellers">Ladakh with Turtuk</a>
        </div>
      </li>
      <li>
        <a href="#trips">Biking Trips <span class="arrow">▾</span></a>
        <div class="dropdown">
          <a href="#trips">Spiti Valley Bike</a>
          <a href="#trips">Ladakh Bike</a>
          <a href="#trips">Tawang Bike</a>
          <a href="#trips">Bhutan Bike</a>
        </div>
      </li>
      <li>
        <a href="#treks">Himalayan Treks</a>
      </li>
      <li>
        <a href="#trips">International</a>
      </li>
      <li>
        <a href="#upcoming">Upcoming</a>
      </li>
      <li>
        <a href="#contact">More <span class="arrow">▾</span></a>
        <div class="dropdown">
          <a href="#about">About Us</a>
          <a href="#contact">Contact</a>
          <a href="#blogs">Blogs</a>
          <a href="#">All Girls Trips</a>
          <a href="#">Honeymoon Trips</a>
          <a href="#">Corporate & MICE</a>
        </div>
      </li>
    </ul>

    <div class="nav-actions">
      <a href="tel:+919797972175" class="nav-phone">📞 +91 97979 72175</a>
      <button class="btn-login">Login</button>
      <button class="btn-book">Book Now</button>
      <button class="ham" id="hamBtn" aria-label="Menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</nav>

<!-- Mobile Menu -->
<div class="mobile-menu" id="mobileMenu">
  <span class="mm-section">Group Trips</span>
  <a href="#trips">🏔 Backpacking Trips</a>
  <a href="#treks">🥾 Himalayan Treks</a>
  <a href="#trips">🏍 Biking Trips</a>
  <a href="#bestsellers">⭐ Best Sellers</a>
  <a href="#trips">🌍 International Trips</a>
  <a href="#upcoming">📅 Upcoming Trips</a>
  <span class="mm-section">Customized</span>
  <a href="#">🏠 Domestic Tours</a>
  <a href="#">✈️ International Getaways</a>
  <a href="#">💑 Honeymoon Trips</a>
  <a href="#">🏢 Corporate & MICE</a>
  <span class="mm-section">Company</span>
  <a href="#about">About Us</a>
  <a href="#blogs">Our Blogs</a>
  <a href="#contact">Contact Us</a>
</div>

<!-- ═══ HERO ═══ -->
<section class="hero" style="margin-top: 0; padding-top: var(--nav-h);">
  <div class="hero-slides" id="heroSlides">
    <div class="hero-slide active"></div>
    <div class="hero-slide"></div>
    <div class="hero-slide"></div>
    <div class="hero-slide"></div>
    <div class="hero-slide"></div>
  </div>
  <div class="hero-content">
    <p class="hero-subtitle fade-up fade-up-d1">India's Premier Travel Community</p>
    <h1 class="hero-title fade-up fade-up-d2">Book Your Trip to</h1>
    <div class="hero-places fade-up fade-up-d3">
      <div class="hero-places-inner" id="heroPlaces">
        <div>Ladakh</div>
        <div>Spiti Valley</div>
        <div>Bali</div>
        <div>Kashmir</div>
        <div>Bhutan</div>
        <div>Meghalaya</div>
        <div>Ladakh</div>
      </div>
    </div>
    <p class="hero-tagline fade-up fade-up-d3">Wander · Travel · Connect · Repeat &nbsp;|&nbsp; Where Adventure meets Community</p>
    <div class="hero-cta fade-up fade-up-d4">
      <a href="#trips" class="cta-primary">Explore Trips</a>
      <a href="#contact" class="cta-secondary">Talk to an Expert</a>
    </div>
  </div>
  <div class="hero-dots" id="heroDots">
    <div class="hero-dot active"></div>
    <div class="hero-dot"></div>
    <div class="hero-dot"></div>
    <div class="hero-dot"></div>
    <div class="hero-dot"></div>
  </div>
</section>

<!-- ═══ STATS STRIP ═══ -->
<div class="stats-strip">
  <div class="stats-inner">
    <div class="stat-item">
      <span class="stat-num">50,000+</span>
      <div class="stat-label">Satisfied Travellers</div>
    </div>
    <div class="stat-item">
      <span class="stat-num">10,000+</span>
      <div class="stat-label">5-Star Reviews</div>
    </div>
    <div class="stat-item">
      <span class="stat-num">50+</span>
      <div class="stat-label">Destinations</div>
    </div>
    <div class="stat-item">
      <span class="stat-num">7 Years+</span>
      <div class="stat-label">Experience</div>
    </div>
  </div>
</div>

<!-- ═══ CATEGORIES ═══ -->
<section class="section section-alt">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Explore by Type</div>
      <h2 class="section-title">What kind of traveller are you?</h2>
    </div>
    <div class="category-grid">
      <a href="#trips" class="category-item">
        <div class="cat-icon">🌟</div>
        <span class="cat-label">New Launches</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">🌍</div>
        <span class="cat-label">International</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">🏔</div>
        <span class="cat-label">Ladakh</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">🗻</div>
        <span class="cat-label">Spiti</span>
      </a>
      <a href="#treks" class="category-item">
        <div class="cat-icon">🥾</div>
        <span class="cat-label">Treks</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">🏍</div>
        <span class="cat-label">Biking</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">👩‍🤝‍👩</div>
        <span class="cat-label">All Girls</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">💑</div>
        <span class="cat-label">Honeymoon</span>
      </a>
      <a href="#trips" class="category-item">
        <div class="cat-icon">✏️</div>
        <span class="cat-label">Customized</span>
      </a>
    </div>
  </div>
</section>

<!-- ═══ TRIPS ═══ -->
<section class="section" id="trips">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Group Departures</div>
      <h2 class="section-title">Trending Trips</h2>
    </div>
    <div class="tabs" id="tripTabs">
      <button class="tab active" data-tab="domestic">Domestic</button>
      <button class="tab" data-tab="international">International</button>
    </div>
    <div id="tripCards">
      <div class="cards-grid">

        <a href="#" class="trip-card">
          <div class="card-img-wrap">
            <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&q=80" alt="Ladakh"/>
            <div class="card-badge">⭐ Best Seller</div>
          </div>
          <div class="card-body">
            <div class="card-title">Leh Ladakh with Turtuk – 7 Days</div>
            <div class="card-meta">
              Leh to Leh <span class="card-dot"></span> 6N/7D <span class="card-dot"></span> Jun – Oct
            </div>
            <div class="card-price">
              <span class="card-price-current">₹ 36,000</span>
              <span class="card-price-old">₹ 42,000</span>
              <span class="card-price-discount">Save ₹6k</span>
            </div>
          </div>
        </a>

        <a href="#" class="trip-card">
          <div class="card-img-wrap">
            <img src="https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=600&q=80" alt="Spiti"/>
          </div>
          <div class="card-body">
            <div class="card-title">Spiti Valley Bike & Backpacking Trip</div>
            <div class="card-meta">
              Manali to Shimla <span class="card-dot"></span> 8N/9D <span class="card-dot"></span> Jun – Sep
            </div>
            <div class="card-price">
              <span class="card-price-current">₹ 28,000</span>
            </div>
          </div>
        </a>

        <a href="#" class="trip-card">
          <div class="card-img-wrap">
            <img src="https://images.unsplash.com/photo-1590523741831-ab7e8b8f9c7f?w=600&q=80" alt="Kashmir"/>
            <div class="card-badge">🔥 Popular</div>
          </div>
          <div class="card-body">
            <div class="card-title">Kashmir Great Lakes Trek – 7 Days</div>
            <div class="card-meta">
              Gagangir to Naranag <span class="card-dot"></span> 6N/7D <span class="card-dot"></span> Jul – Sep
            </div>
            <div class="card-price">
              <span class="card-price-current">₹ 18,500</span>
              <span class="card-price-old">₹ 20,000</span>
              <span class="card-price-discount">Save ₹1.5k</span>
            </div>
          </div>
        </a>

        <a href="#" class="trip-card">
          <div class="card-img-wrap">
            <img src="https://images.unsplash.com/photo-1501854140801-50d01698950b?w=600&q=80" alt="Valley of Flowers"/>
          </div>
          <div class="card-body">
            <div class="card-title">Valley of Flowers Trek – 6 Days</div>
            <div class="card-meta">
              Rishikesh to Rishikesh <span class="card-dot"></span> 5N/6D <span class="card-dot"></span> Jul – Aug
            </div>
            <div class="card-price">
              <span class="card-price-current">₹ 11,000</span>
              <span class="card-price-old">₹ 12,500</span>
              <span class="card-price-discount">Save ₹1.5k</span>
            </div>
          </div>
        </a>

      </div>
    </div>
    <div class="view-all-wrap">
      <a href="#" class="btn-view-all">View All Trips →</a>
    </div>
  </div>
</section>

<!-- ═══ PROMO BANNER ═══ -->
<div class="section-inner" style="max-width:1280px; margin: 0 auto; padding: 0 24px 48px;">
  <div class="promo-banner">
    <h3>Explore <span>International</span> Destinations with Curated Group Tours</h3>
    <a href="#bestsellers" class="promo-btn">View International →</a>
  </div>
</div>

<!-- ═══ BEST SELLERS ═══ -->
<section class="section section-alt" id="bestsellers">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Top Picks</div>
      <h2 class="section-title">Best Sellers</h2>
    </div>
    <div class="tabs">
      <button class="tab active">International</button>
      <button class="tab">Backpacking</button>
      <button class="tab">Biking</button>
      <button class="tab">Treks</button>
    </div>
    <div class="cards-grid">

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1537953773345-d172ccf13cf1?w=600&q=80" alt="Bali"/>
          <div class="card-badge">🌴 New</div>
        </div>
        <div class="card-body">
          <div class="card-title">Bali with Gili Island Group Tour – 7N/8D</div>
          <div class="card-meta">
            Bali Airport to Bali <span class="card-dot"></span> 7N/8D <span class="card-dot"></span> Jun – Aug
          </div>
          <div class="card-price">
            <span class="card-price-current">₹ 52,500</span>
            <span class="card-price-old">₹ 56,000</span>
            <span class="card-price-discount">Save ₹3.5k</span>
          </div>
        </div>
      </a>

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600&q=80" alt="Thailand"/>
          <div class="card-badge">🔥 Hot Deal</div>
        </div>
        <div class="card-body">
          <div class="card-title">Thailand Full Moon Party Group Tour</div>
          <div class="card-meta">
            Phuket to Phuket <span class="card-dot"></span> 6N/7D <span class="card-dot"></span> May – Sep
          </div>
          <div class="card-price">
            <span class="card-price-current">₹ 52,000</span>
            <span class="card-price-old">₹ 57,000</span>
            <span class="card-price-discount">Save ₹5k</span>
          </div>
        </div>
      </a>

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1524492412937-b28074a5d7da?w=600&q=80" alt="Bhutan"/>
        </div>
        <div class="card-body">
          <div class="card-title">Bhutan Bike & Backpacking – 8 Days Bhutan Bike Tour</div>
          <div class="card-meta">
            Bagdogra to Bagdogra <span class="card-dot"></span> 7N/8D <span class="card-dot"></span> Sep – May
          </div>
          <div class="card-price">
            <span class="card-price-current">₹ 45,000</span>
          </div>
        </div>
      </a>

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&q=80" alt="Vietnam"/>
        </div>
        <div class="card-body">
          <div class="card-title">Vietnam Heritage Group Tour – 8N/9D</div>
          <div class="card-meta">
            Hanoi to Ho Chi Minh <span class="card-dot"></span> 8N/9D <span class="card-dot"></span> Oct – Mar
          </div>
          <div class="card-price">
            <span class="card-price-current">₹ 48,000</span>
          </div>
        </div>
      </a>

    </div>
    <div class="view-all-wrap">
      <a href="#" class="btn-view-all">View All Best Sellers →</a>
    </div>
  </div>
</section>

<!-- ═══ UPCOMING TRIPS ═══ -->
<section class="section" id="upcoming">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Don't Miss Out</div>
      <h2 class="section-title">Upcoming Trips</h2>
    </div>
    <div class="tabs">
      <button class="tab active">Domestic</button>
      <button class="tab">International</button>
    </div>
    <div class="upcoming-grid">
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">14</div><div class="month">Jun</div></div>
        <div><div class="upcoming-name">Leh Ladakh with Turtuk – Nubra Circuit</div><div class="upcoming-dur">8N/9D &nbsp;·&nbsp; Leh to Leh</div></div>
        <div class="upcoming-seats">12 seats left</div>
        <div class="upcoming-price">₹36,000</div>
      </a>
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">21</div><div class="month">Jun</div></div>
        <div><div class="upcoming-name">Spiti Valley Road Trip</div><div class="upcoming-dur">7N/8D &nbsp;·&nbsp; Manali to Shimla</div></div>
        <div class="upcoming-seats">8 seats left</div>
        <div class="upcoming-price">₹28,000</div>
      </a>
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">05</div><div class="month">Jul</div></div>
        <div><div class="upcoming-name">Valley of Flowers Trek</div><div class="upcoming-dur">5N/6D &nbsp;·&nbsp; Rishikesh</div></div>
        <div class="upcoming-seats">20 seats left</div>
        <div class="upcoming-price">₹11,000</div>
      </a>
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">12</div><div class="month">Jul</div></div>
        <div><div class="upcoming-name">Kashmir Great Lakes Trek</div><div class="upcoming-dur">6N/7D &nbsp;·&nbsp; Gagangir to Naranag</div></div>
        <div class="upcoming-seats">5 seats left</div>
        <div class="upcoming-price">₹18,500</div>
      </a>
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">20</div><div class="month">Jul</div></div>
        <div><div class="upcoming-name">Meghalaya Monsoon Group Trip</div><div class="upcoming-dur">5N/6D &nbsp;·&nbsp; Guwahati to Guwahati</div></div>
        <div class="upcoming-seats">15 seats left</div>
        <div class="upcoming-price">₹24,000</div>
      </a>
      <a href="#" class="upcoming-item">
        <div class="upcoming-date"><div class="day">02</div><div class="month">Aug</div></div>
        <div><div class="upcoming-name">Hampta Pass Trek</div><div class="upcoming-dur">4N/5D &nbsp;·&nbsp; Manali</div></div>
        <div class="upcoming-seats">18 seats left</div>
        <div class="upcoming-price">₹11,000</div>
      </a>
    </div>
    <div class="view-all-wrap">
      <a href="#" class="btn-view-all">View All Upcoming Trips →</a>
    </div>
  </div>
</section>

<!-- ═══ HIMALAYAN TREKS ═══ -->
<section class="section section-alt" id="treks">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Into the Mountains</div>
      <h2 class="section-title">Himalayan Treks</h2>
    </div>
    <div class="tabs">
      <button class="tab active">Monsoon Treks</button>
      <button class="tab">Summer Treks</button>
    </div>
    <div class="cards-grid">

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=600&q=80" alt="Hampta Pass"/>
          <div class="card-badge">🥾 Top Trek</div>
        </div>
        <div class="card-body">
          <div class="card-title">Hampta Pass Trek – 5 Days</div>
          <div class="card-meta">Manali to Manali <span class="card-dot"></span> 4N/5D <span class="card-dot"></span> Jun – Sep</div>
          <div class="card-price">
            <span class="card-price-current">₹ 11,000</span>
            <span class="card-price-old">₹ 12,500</span>
            <span class="card-price-discount">Save ₹1.5k</span>
          </div>
        </div>
      </a>

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1501854140801-50d01698950b?w=600&q=80" alt="Valley of Flowers"/>
        </div>
        <div class="card-body">
          <div class="card-title">Valley of Flowers Trek</div>
          <div class="card-meta">Rishikesh to Rishikesh <span class="card-dot"></span> 5N/6D <span class="card-dot"></span> Jul – Aug</div>
          <div class="card-price">
            <span class="card-price-current">₹ 11,000</span>
            <span class="card-price-old">₹ 12,000</span>
            <span class="card-price-discount">Save ₹1k</span>
          </div>
        </div>
      </a>

      <a href="#" class="trip-card">
        <div class="card-img-wrap">
          <img src="https://images.unsplash.com/photo-1455156218388-5e61b526818b?w=600&q=80" alt="Kashmir Great Lakes"/>
        </div>
        <div class="card-body">
          <div class="card-title">Kashmir Great Lakes Trek</div>
          <div class="card-meta">Gagangir to Naranag <span class="card-dot"></span> 6N/7D <span class="card-dot"></span> Jul – Sep</div>
          <div class="card-price">
            <span class="card-price-current">₹ 18,500</span>
            <span class="card-price-old">₹ 20,000</span>
            <span class="card-price-discount">Save ₹1.5k</span>
          </div>
        </div>
      </a>

    </div>
    <div class="view-all-wrap">
      <a href="#" class="btn-view-all">View All Treks →</a>
    </div>
  </div>
</section>

<!-- ═══ REVIEWS ═══ -->
<section class="section" id="reviews">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Reviews</div>
      <h2 class="section-title">What our Clients Say About Us</h2>
    </div>
    <div class="reviews-grid">

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Our Spiti bike and backpacking trip was an incredible experience, flawlessly organised and well managed. Huge appreciation to the team for handling such a large group so smoothly. Special thanks to the captains for their dedication and genuine care!"</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=600&q=80" alt="Spiti Trip"/>
        <a href="#" class="try-link">Spiti Valley Bike Trip →</a>
        <div class="review-author">
          <div class="review-avatar">R</div>
          <div><div class="review-name">Rehna R Nambiar</div><div class="review-trip">Spiti Valley Bike & Backpacking</div></div>
        </div>
      </div>

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"This was my first trip with LuxeTrail and it turned out to be an amazing trip to Ladakh. The team is committed to providing excellence. The journey plan, stay and food — all beyond expectation and value for money. Truly a great experience!"</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&q=80" alt="Ladakh Trip"/>
        <a href="#" class="try-link">Ladakh with Turtuk →</a>
        <div class="review-author">
          <div class="review-avatar">K</div>
          <div><div class="review-name">Khushboo Kumari</div><div class="review-trip">Leh Hanle Ladakh Trip</div></div>
        </div>
      </div>

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"We booked a honeymoon Bali trip with LuxeTrail. The team handled everything perfectly. My wife and I created long-lasting memories together. Everything was well planned — this is the best trip of my life!"</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1537953773345-d172ccf13cf1?w=600&q=80" alt="Bali Trip"/>
        <a href="#" class="try-link">Bali Honeymoon Package →</a>
        <div class="review-author">
          <div class="review-avatar">S</div>
          <div><div class="review-name">Sachin Sahu</div><div class="review-trip">Bali Honeymoon Tour</div></div>
        </div>
      </div>

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"I had a wonderful experience traveling to Bhutan with LuxeTrail. The trip was well-organized, our host and guide were extremely warm, knowledgeable, and made the journey truly memorable. The accommodations were comfortable and thoughtfully chosen."</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1524492412937-b28074a5d7da?w=600&q=80" alt="Bhutan Trip"/>
        <a href="#" class="try-link">Bhutan Tour →</a>
        <div class="review-author">
          <div class="review-avatar">S</div>
          <div><div class="review-name">Shailja Devgan</div><div class="review-trip">Bhutan Bike & Backpacking</div></div>
        </div>
      </div>

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Had a wonderful experience with LuxeTrail for Thailand. Within 48 hours, they booked our entire trip. They have 24x7 support with immediate responses. It was a smooth travel experience from start to finish. I would definitely go with them again!"</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600&q=80" alt="Thailand Trip"/>
        <a href="#" class="try-link">Thailand Full Moon Party →</a>
        <div class="review-author">
          <div class="review-avatar">P</div>
          <div><div class="review-name">Sai Pradeep</div><div class="review-trip">Thailand Group Tour</div></div>
        </div>
      </div>

      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Booking Bali was always a dream, and LuxeTrail made it exceed every expectation. From the moment we landed until departure, the trip was seamless, stunning, and perfectly managed. I highly recommend this incredible company to everyone!"</p>
        <img class="review-img-trip" src="https://images.unsplash.com/photo-1537953773345-d172ccf13cf1?w=600&q=80" alt="Bali"/>
        <a href="#" class="try-link">Bali with Gili Island →</a>
        <div class="review-author">
          <div class="review-avatar">A</div>
          <div><div class="review-name">Aaditi Bhosale</div><div class="review-trip">Bali Group Tour</div></div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ═══ WHY US ═══ -->
<section class="section section-alt">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Why Choose Us</div>
      <h2 class="section-title">The LuxeTrail Difference</h2>
    </div>
    <div class="why-grid">
      <div class="why-card">
        <div class="why-icon">🛡️</div>
        <div class="why-title">Free Travel Insurance</div>
        <div class="why-desc">Every traveller covered with free adventure travel insurance up to ₹4.5 Lakhs on all trips.</div>
      </div>
      <div class="why-card">
        <div class="why-icon">🏅</div>
        <div class="why-title">Certified Trip Leaders</div>
        <div class="why-desc">All leaders hold AMC/BMC certifications with first-aid training ensuring maximum safety.</div>
      </div>
      <div class="why-card">
        <div class="why-icon">🏍️</div>
        <div class="why-title">Free Riding Gear</div>
        <div class="why-desc">Complimentary riding jacket and gear for all biking trips. Ride safe, ride in style.</div>
      </div>
      <div class="why-card">
        <div class="why-icon">👥</div>
        <div class="why-title">Community First</div>
        <div class="why-desc">Travel with like-minded explorers. Find your tribe and create lifelong friendships.</div>
      </div>
      <div class="why-card">
        <div class="why-icon">📞</div>
        <div class="why-title">24/7 On-Ground Support</div>
        <div class="why-desc">100+ strong on-ground team with round-the-clock local support at every destination.</div>
      </div>
      <div class="why-card">
        <div class="why-icon">✈️</div>
        <div class="why-title">Customized Itineraries</div>
        <div class="why-desc">Hand-picked, expert-curated itineraries tailored to give you the best possible experience.</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══ ABOUT ═══ -->
<section class="section" id="about">
  <div class="section-inner">
    <div class="about-wrap">
      <div class="about-img-grid">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800&q=80" alt="Mountain Trek"/>
        <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=400&q=80" alt="Ladakh"/>
        <img src="https://images.unsplash.com/photo-1537953773345-d172ccf13cf1?w=400&q=80" alt="Bali"/>
      </div>
      <div class="about-text">
        <div class="section-eyebrow">Our Story</div>
        <h2 class="section-title" style="margin-bottom: 20px;">India's Most Trusted Travel Community</h2>
        <p>LuxeTrail Holidays was born from a simple belief — that travel is the greatest teacher. Founded with the mission of making extraordinary journeys accessible to every adventurer, we've spent years crafting experiences that don't just take you to a destination, but transform you along the way.</p>
        <p>From the snow-dusted passes of Ladakh to the turquoise waters of Bali, we've curated over 50 destinations for 50,000+ travellers. Our community of Luxe Explorers spans every corner of India, united by a shared passion for the road less travelled.</p>
        <p>As an ATOAI-registered operator, safety is our founding principle. Every trip leader is a certified expert. Every itinerary is meticulously planned. And every memory we help you create is built to last a lifetime.</p>
        <div class="about-stats">
          <div class="about-stat-item"><span class="about-stat-num">50,000+</span><div class="about-stat-label">Happy Travellers</div></div>
          <div class="about-stat-item"><span class="about-stat-num">250+</span><div class="about-stat-label">Customized Tours</div></div>
          <div class="about-stat-item"><span class="about-stat-num">50+</span><div class="about-stat-label">Group Tours</div></div>
          <div class="about-stat-item"><span class="about-stat-num">10,000+</span><div class="about-stat-label">Reviews</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══ FAQ ═══ -->
<section class="section section-alt">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">FAQ</div>
      <h2 class="section-title">Have any Doubts?</h2>
    </div>
    <div class="faq-list">
      <div class="faq-item open">
        <button class="faq-q">What does LuxeTrail Holidays offer? <span class="faq-icon">+</span></button>
        <div class="faq-a">LuxeTrail Holidays offers group departures to North India and North East India, bike and backpacking trips, weekend getaways, All Girls trips, International escapes, Himalayan treks, Corporate tours, and customised international and domestic tours for all types of travellers.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">Can I join as a solo traveller? <span class="faq-icon">+</span></button>
        <div class="faq-a">Absolutely! Many of our travellers join group departures as solo explorers and find their tribe during the journey. Our hand-picked stay options and carefully curated itineraries ensure you get both amazing group experiences and personal time for yourself.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">How experienced are LuxeTrail's Trip Leaders? <span class="faq-icon">+</span></button>
        <div class="faq-a">All key trip leaders are certified with AMC or BMC qualifications and are trained in first-aid procedures to ensure the safety of all travellers. They are seasoned experts who know the terrain, weather patterns, and how to handle any situation that may arise on the trail.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">What are All Girls Trips? <span class="faq-icon">+</span></button>
        <div class="faq-a">All Girls Trips are a unique offering where women from different backgrounds come together to explore incredible destinations. Each trip is headed by a female trip leader who is an experienced expert. Safety, comfort, and unforgettable experiences are all guaranteed.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">How do I book a trip with LuxeTrail? <span class="faq-icon">+</span></button>
        <div class="faq-a">Booking is simple — browse our trips, select your preferred package, review the itinerary details, and proceed to the booking section. Pay a small advance to confirm your spot, and the confirmation email will serve as your ticket to adventure. Our team will guide you through every step.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">What international destinations does LuxeTrail cover? <span class="faq-icon">+</span></button>
        <div class="faq-a">We actively curate trips to Bali, Thailand, Bhutan, Vietnam, Dubai, Maldives, Sri Lanka, Nepal, and more. Check our International Trips section for the latest departures, group tours, and customised packages across all these destinations.</div>
      </div>
      <div class="faq-item">
        <button class="faq-q">Is travel insurance provided? <span class="faq-icon">+</span></button>
        <div class="faq-a">Yes! LuxeTrail Holidays provides complimentary travel insurance for adventure activities up to ₹4.5 Lakhs for every traveller. Being the first in our segment to offer this, your safety and peace of mind is our highest priority on every journey.</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══ BLOGS ═══ -->
<section class="section" id="blogs">
  <div class="section-inner">
    <div class="section-header">
      <div class="section-eyebrow">Blogs</div>
      <h2 class="section-title">Our Blogs</h2>
    </div>
    <div class="blog-grid">
      <a href="#" class="blog-card">
        <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&q=80" alt="Blog"/>
        <div class="blog-body">
          <div class="blog-date">May 10, 2025 &nbsp;·&nbsp; 7 min read</div>
          <div class="blog-title">Why LuxeTrail is the Perfect Choice for Your All-Girls Trip</div>
          <div class="blog-read">Read More →</div>
        </div>
      </a>
      <a href="#" class="blog-card">
        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=600&q=80" alt="Blog"/>
        <div class="blog-body">
          <div class="blog-date">Apr 20, 2025 &nbsp;·&nbsp; 5 min read</div>
          <div class="blog-title">Book Now, Pay Later – Travel Now, Pay in Easy EMIs with LuxeTrail</div>
          <div class="blog-read">Read More →</div>
        </div>
      </a>
      <a href="#" class="blog-card">
        <img src="https://images.unsplash.com/photo-1501854140801-50d01698950b?w=600&q=80" alt="Blog"/>
        <div class="blog-body">
          <div class="blog-date">Apr 8, 2025 &nbsp;·&nbsp; 23 min read</div>
          <div class="blog-title">25 Best Places to Visit in June in India – 2025 Travel Guide</div>
          <div class="blog-read">Read More →</div>
        </div>
      </a>
    </div>
    <div class="view-all-wrap">
      <a href="#" class="btn-view-all">View All Blogs →</a>
    </div>
  </div>
</section>

<!-- ═══ RECOGNITIONS ═══ -->
<section class="section section-alt">
  <div class="section-inner">
    <div class="section-header" style="text-align:center;">
      <div class="section-eyebrow">Our Recognitions</div>
      <h2 class="section-title">Recognised by Government & Industry Leaders</h2>
    </div>
    <div class="recog-strip">
      <div class="recog-badge"><span>🏆</span> Startup India</div>
      <div class="recog-badge"><span>🏅</span> MSME Best Enterprise</div>
      <div class="recog-badge"><span>⭐</span> TripAdvisor Travellers' Choice</div>
      <div class="recog-badge"><span>🌐</span> ATOAI Member</div>
      <div class="recog-badge"><span>🏛</span> UP Tourism Recognised</div>
      <div class="recog-badge"><span>🎓</span> IIM Bangalore Incubated</div>
      <div class="recog-badge"><span>🔍</span> Google For Startups</div>
      <div class="recog-badge"><span>📰</span> Business Standard Featured</div>
    </div>
  </div>
</section>

<!-- ═══ NEWSLETTER ═══ -->
<section class="section" id="contact">
  <div class="section-inner">
    <div class="newsletter">
      <div>
        <h2>Stay in the Loop 🌏</h2>
        <p>Be the first to know about exciting offers, new trip launches, and travel updates.</p>
      </div>
      <div class="newsletter-form">
        <input type="email" placeholder="Enter your email address"/>
        <button>Subscribe Now</button>
      </div>
    </div>
  </div>
</section>

<!-- ═══ FOOTER ═══ -->
<footer>
  <div class="footer-inner">
    <div class="footer-brand">
      <a href="#" class="logo" style="text-decoration:none;">
        <div class="logo-icon"><svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg></div>
        <div class="logo-text"><span>LuxeTrail</span> Holidays</div>
      </a>
      <p>India's premium travel community for group trips, treks & custom tours. Trusted by 50,000+ explorers with free ₹4.5L insurance & expert guides.</p>
      <div class="footer-contact">
        <a href="tel:+919797972175">📞 +91 97979 72175</a>
        <a href="mailto:hello@luxetrailholidays.com">✉️ hello@luxetrailholidays.com</a>
        <a href="#">📍 New Delhi, India</a>
      </div>
      <div class="footer-socials">
        <a href="#" class="social-btn">f</a>
        <a href="#" class="social-btn">in</a>
        <a href="#" class="social-btn">▶</a>
        <a href="#" class="social-btn">ig</a>
        <a href="#" class="social-btn">tw</a>
      </div>
    </div>

    <div class="footer-col">
      <h4>Company</h4>
      <ul>
        <li><a href="#about">About Us</a></li>
        <li><a href="#contact">Contact Us</a></li>
        <li><a href="#blogs">Our Blogs</a></li>
        <li><a href="#">Careers</a></li>
        <li><a href="#">Newsletter</a></li>
        <li><a href="#">Payment Policy</a></li>
      </ul>
    </div>

    <div class="footer-col">
      <h4>Group Tours</h4>
      <ul>
        <li><a href="#trips">Backpacking Trips</a></li>
        <li><a href="#treks">Himalayan Treks</a></li>
        <li><a href="#trips">Biking Trips</a></li>
        <li><a href="#upcoming">Upcoming Trips</a></li>
        <li><a href="#bestsellers">International Trips</a></li>
        <li><a href="#">All Girls Trips</a></li>
      </ul>
    </div>

    <div class="footer-col">
      <h4>Customized Trips</h4>
      <ul>
        <li><a href="#">Corporate Tours</a></li>
        <li><a href="#">Domestic Tours</a></li>
        <li><a href="#">International Getaways</a></li>
        <li><a href="#">Honeymoon Trips</a></li>
        <li><a href="#">School Tours</a></li>
        <li><a href="#">Weekend Getaways</a></li>
      </ul>
    </div>
  </div>

  <div style="max-width:1280px; margin: 0 auto; padding: 0 24px;">
    <div class="footer-bottom">
      <span class="footer-bottom-copy">© 2024–2025 LuxeTrail Holidays. All rights reserved.</span>
      <div class="footer-bottom-links">
        <a href="#">Privacy Policy</a>
        <a href="#">Terms & Conditions</a>
        <a href="#">Refund Policy</a>
      </div>
    </div>
  </div>
</footer>

<script>
// ─── HERO SLIDER ───
let heroSlide = 0;
const slides = document.querySelectorAll('.hero-slide');
const dots = document.querySelectorAll('.hero-dot');
function goSlide(n) {
  slides[heroSlide].classList.remove('active');
  dots[heroSlide].classList.remove('active');
  heroSlide = (n + slides.length) % slides.length;
  slides[heroSlide].classList.add('active');
  dots[heroSlide].classList.add('active');
}
setInterval(() => goSlide(heroSlide + 1), 4500);
dots.forEach((d,i) => d.addEventListener('click', () => goSlide(i)));

// ─── HERO PLACE ROTATOR ───
let placeIdx = 0;
const placesInner = document.getElementById('heroPlaces');
const placeItems = placesInner.children;
setInterval(() => {
  placeIdx++;
  if (placeIdx >= placeItems.length - 1) placeIdx = 0;
  placesInner.style.transform = `translateY(-${placeIdx * 100}%)`;
}, 2200);

// ─── HAMBURGER ───
const hamBtn = document.getElementById('hamBtn');
const mobileMenu = document.getElementById('mobileMenu');
hamBtn.addEventListener('click', () => {
  mobileMenu.classList.toggle('open');
});

// ─── FAQ ACCORDION ───
document.querySelectorAll('.faq-q').forEach(btn => {
  btn.addEventListener('click', () => {
    const item = btn.parentElement;
    const isOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item').forEach(i => i.classList.remove('open'));
    if (!isOpen) item.classList.add('open');
  });
});

// ─── TABS (Visual only) ───
document.querySelectorAll('.tabs').forEach(tabsEl => {
  tabsEl.querySelectorAll('.tab').forEach(tab => {
    tab.addEventListener('click', () => {
      tabsEl.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
      tab.classList.add('active');
    });
  });
});

// ─── NEWSLETTER ───
const newsForm = document.querySelector('.newsletter-form');
newsForm.querySelector('button').addEventListener('click', () => {
  const input = newsForm.querySelector('input');
  if (input.value && input.value.includes('@')) {
    newsForm.innerHTML = '<p style="color:#f5c842;font-weight:600;font-size:1rem;">🎉 You\'re subscribed! Welcome to the LuxeTrail family.</p>';
  } else {
    input.style.border = '2px solid #e8521a';
    input.placeholder = 'Please enter a valid email!';
  }
});

// ─── SMOOTH SCROLL FIX ───
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    const target = document.querySelector(a.getAttribute('href'));
    if (target) {
      e.preventDefault();
      window.scrollTo({ top: target.offsetTop - 80, behavior: 'smooth' });
      mobileMenu.classList.remove('open');
    }
  });
});
</script>
</body>
</html>
