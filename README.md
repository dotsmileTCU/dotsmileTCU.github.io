<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>多彩梦交通文化综合体</title>
<style>
  /* =========================================================
     全局
     ========================================================= */
  * { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --primary: #1e3a5f;
    --primary-light: #2c5282;
    --accent: #e8a838;
    --accent-dark: #c98a1e;
    --text: #1a1a2e;
    --text-light: #666;
    --bg: #f7f8fa;
    --card-bg: #fff;
    --border: #e5e7eb;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC",
                 "Microsoft YaHei", sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    min-height: 100vh;
  }

  a { color: inherit; }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 24px;
  }

  /* =========================================================
     顶部导航
     ========================================================= */
  .navbar {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(255, 255, 255, 0.94);
    backdrop-filter: saturate(180%) blur(12px);
    -webkit-backdrop-filter: saturate(180%) blur(12px);
    border-bottom: 1px solid var(--border);
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 32px;
  }

  .nav-logo {
    font-size: 18px;
    font-weight: 800;
    color: var(--primary);
    text-decoration: none;
    letter-spacing: 1px;
    white-space: nowrap;
  }

  .nav-menu {
    display: flex;
    align-items: center;
    gap: 4px;
  }

  .nav-link {
    padding: 8px 16px;
    border-radius: 6px;
    text-decoration: none;
    color: var(--text);
    font-size: 15px;
    font-weight: 500;
    cursor: pointer;
    transition: background 0.2s, color 0.2s;
    white-space: nowrap;
    border: none;
    background: transparent;
    font-family: inherit;
    display: block;
    text-align: left;
  }
  .nav-link:hover { background: #eef3fa; color: var(--primary); }
  .nav-link.active { color: var(--primary); font-weight: 700; }

  /* 汉堡菜单 */
  .hamburger-wrap { position: relative; }

  .hamburger-btn {
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 6px;
    cursor: pointer;
    border: none;
    background: transparent;
    transition: background 0.2s;
  }
  .hamburger-btn:hover { background: #eef3fa; }
  .hamburger-btn svg {
    width: 22px; height: 22px;
    stroke: var(--text); stroke-width: 2;
    fill: none; stroke-linecap: round;
  }

  .hamburger-dropdown {
    position: absolute;
    top: 100%;
    right: 0;
    margin-top: 6px;
    min-width: 180px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 8px 28px rgba(0, 0, 0, 0.12);
    padding: 8px;
    opacity: 0;
    visibility: hidden;
    transform: translateY(-6px);
    transition: opacity 0.2s, transform 0.2s, visibility 0.2s;
  }
  .hamburger-wrap:hover .hamburger-dropdown,
  .hamburger-dropdown.show {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
  }
  .hamburger-dropdown .nav-link { padding: 10px 14px; }

  @media (max-width: 820px) {
    .navbar { padding: 0 16px; }
    .nav-link.primary-link { display: none; }
    .nav-logo { font-size: 15px; }
  }

  /* =========================================================
     页面容器
     ========================================================= */
  .page { display: none; }
  .page.active { display: block; animation: fadeUp 0.35s ease; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(10px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* =========================================================
     页面 1：组织简介
     ========================================================= */

     .top-btn-wrap {
     text-align: center;
     margin-bottom: 40px;
     }
     .top-btn {
     display: inline-block;
     padding: 14px 48px;
     background: #1e3a5f;
     color: #fff;
     font-size: 18px;
     font-weight: 600;
     text-decoration: none;
     border-radius: 8px;
     transition: background 0.25s, transform 0.15s;
     box-shadow: 0 4px 14px rgba(30, 58, 95, 0.25);
     }
     .top-btn:hover {
     background: #2c5282;
     transform: translateY(-2px);
     }
     .top-btn:active {
     transform: translateY(0);
     }

</style>
</head>
<body>
<!-- ============================================================
     第一部分：顶部按钮 —— “找到我们”
<div class="top-btn-wrap">
  <a class="top-btn" href="https://metro-lingnandongdao.github.io/lingnan-portfolio/sites.html">
    找到我们
  </a>
</div>

  .home-hero {
    padding: 100px 0 70px;
    background: linear-gradient(160deg, #f7f8fa 0%, #e9eef5 100%);
    border-bottom: 1px solid var(--border);
  }
  .home-hero-tag {
    display: inline-block;
    padding: 4px 14px;
    background: #eef3fa;
    color: var(--primary);
    border-radius: 20px;
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 20px;
  }
  .home-hero h1 {
    font-size: 44px;
    line-height: 1.25;
    font-weight: 800;
    color: var(--primary);
    margin-bottom: 18px;
    letter-spacing: -0.5px;
  }
  .home-hero p {
    font-size: 17px;
    color: var(--text-light);
    max-width: 720px;
    line-height: 1.75;
  }

  .home-split {
    display: grid;
    grid-template-columns: 1.4fr 1fr;
    gap: 60px;
    padding: 70px 0;
    align-items: start;
  }
  @media (max-width: 820px) {
    .home-split { grid-template-columns: 1fr; gap: 40px; }
    .home-hero h1 { font-size: 32px; }
  }

  .home-story h2 {
    font-size: 24px;
    color: var(--primary);
    margin-bottom: 20px;
    position: relative;
    padding-left: 16px;
  }
  .home-story h2::before {
    content: "";
    position: absolute;
    left: 0; top: 50%;
    width: 4px; height: 24px;
    background: var(--accent);
    border-radius: 2px;
    transform: translateY(-50%);
  }
  .home-story p {
    margin-bottom: 16px;
    color: #444;
    font-size: 15px;
    line-height: 1.9;
  }

  .stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .stat-item {
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px 20px;
    text-align: center;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .stat-item:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(30, 58, 95, 0.08);
  }
  .stat-num {
    font-size: 32px;
    font-weight: 800;
    color: var(--primary);
    line-height: 1;
    margin-bottom: 8px;
  }
  .stat-num span { color: var(--accent); font-size: 20px; }
  .stat-label { font-size: 13px; color: var(--text-light); }


  /* 两大常年活动 */
  .annual-section {
    padding: 60px 0 80px;
  }
  .annual-title {
    text-align: center;
    font-size: 28px;
    font-weight: 800;
    color: var(--primary);
    margin-bottom: 8px;
  }
  .annual-subtitle {
    text-align: center;
    font-size: 14px;
    color: #888;
    margin-bottom: 40px;
  }
  .annual-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }
  @media (max-width: 820px) {
    .annual-grid { grid-template-columns: 1fr; }
  }
  .annual-card {
    background: #fff;
    border-radius: 16px;
    padding: 36px 30px;
    border: 1px solid var(--border);
    position: relative;
    overflow: hidden;
    transition: transform 0.25s, box-shadow 0.25s;
  }
  .annual-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 14px 36px rgba(30, 58, 95, 0.12);
  }
  .annual-card::before {
    content: "";
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 5px;
    background: linear-gradient(90deg, var(--accent), var(--primary));
  }
  .annual-card.alt::before {
    background: linear-gradient(90deg, var(--primary), var(--accent));
  }
  .annual-tag {
    display: inline-block;
    font-size: 12px;
    font-weight: 700;
    padding: 3px 12px;
    border-radius: 12px;
    background: #fff4dd;
    color: var(--accent-dark);
    margin-bottom: 16px;
  }
  .annual-card.alt .annual-tag {
    background: #eef3fa;
    color: var(--primary);
  }
  .annual-card h3 {
    font-size: 22px;
    color: var(--primary);
    margin-bottom: 10px;
  }
  .annual-card .annual-time {
    font-size: 14px;
    color: var(--accent-dark);
    font-weight: 600;
    margin-bottom: 14px;
  }
  .annual-card.alt .annual-time {
    color: var(--primary);
  }
  .annual-card p {
    font-size: 14px;
    color: var(--text-light);
    line-height: 1.8;
  }

  /* =========================================================
     页面 2：联系我们
     ========================================================= */
  .contact-hero {
    padding: 80px 0 50px;
    text-align: center;
  }
  .contact-hero h1 {
    font-size: 40px;
    font-weight: 800;
    color: var(--primary);
    margin-bottom: 14px;
    letter-spacing: -0.5px;
  }
  .contact-hero p {
    font-size: 16px;
    color: var(--text-light);
    max-width: 600px;
    margin: 0 auto;
    line-height: 1.75;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    padding: 30px 0 60px;
  }
  .contact-card {
    background: #fff;
    border-radius: 14px;
    padding: 32px 24px;
    text-align: center;
    border: 1px solid var(--border);
    transition: transform 0.2s, box-shadow 0.2s, border-color 0.2s;
  }
  .contact-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 28px rgba(30, 58, 95, 0.1);
    border-color: #cfd9e6;
  }
  .contact-icon {
    font-size: 40px;
    margin-bottom: 16px;
    line-height: 1;
  }
  .contact-card h3 {
    font-size: 17px;
    color: var(--primary);
    margin-bottom: 8px;
  }
  .contact-card p {
    font-size: 14px;
    color: var(--text-light);
    word-break: break-all;
  }

  .contact-cta {
    text-align: center;
    padding: 20px 0 80px;
  }
  .top-btn {
    display: inline-block;
    padding: 14px 48px;
    background: var(--primary);
    color: #fff;
    font-size: 17px;
    font-weight: 600;
    text-decoration: none;
    border-radius: 8px;
    transition: background 0.25s, transform 0.15s, box-shadow 0.25s;
    box-shadow: 0 4px 14px rgba(30, 58, 95, 0.25);
  }
  .top-btn:hover {
    background: var(--primary-light);
    transform: translateY(-2px);
    box-shadow: 0 8px 22px rgba(30, 58, 95, 0.3);
  }

  /* =========================================================
     页面 3：参与共创
     ========================================================= */
  .coop-hero {
    padding: 90px 0 70px;
    background: linear-gradient(150deg, #fff4dd 0%, #ffe7bd 100%);
    text-align: center;
    border-bottom: 1px solid #f0dfb8;
  }
  .coop-hero h1 {
    font-size: 44px;
    font-weight: 800;
    color: #7a4e00;
    margin-bottom: 16px;
    letter-spacing: -0.5px;
  }
  .coop-hero p {
    font-size: 17px;
    color: #8b5e1a;
    max-width: 680px;
    margin: 0 auto;
    line-height: 1.75;
  }

  .coop-steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px;
    padding: 60px 0;
  }
  .coop-step {
    background: #fff;
    border-radius: 14px;
    padding: 32px 26px;
    border-top: 4px solid var(--accent);
    box-shadow: 0 4px 18px rgba(232, 168, 56, 0.08);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .coop-step:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 30px rgba(232, 168, 56, 0.18);
  }
  .coop-step-num {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 40px; height: 40px;
    background: var(--accent);
    color: #fff;
    border-radius: 50%;
    font-weight: 800;
    font-size: 18px;
    margin-bottom: 18px;
  }
  .coop-step h3 {
    font-size: 18px;
    color: #7a4e00;
    margin-bottom: 10px;
  }
  .coop-step p {
    font-size: 14px;
    color: var(--text-light);
    line-height: 1.75;
  }

  .coop-cta-wrap {
    background: #fff;
    border-radius: 16px;
    padding: 48px 32px;
    text-align: center;
    margin: 20px 0 80px;
    box-shadow: 0 4px 24px rgba(0, 0, 0, 0.05);
  }
  .coop-cta-wrap h2 {
    font-size: 26px;
    color: var(--primary);
    margin-bottom: 12px;
  }
  .coop-cta-wrap p {
    color: var(--text-light);
    margin-bottom: 24px;
  }
  .coop-btn {
    display: inline-block;
    padding: 13px 40px;
    background: var(--accent);
    color: #fff;
    font-size: 16px;
    font-weight: 700;
    text-decoration: none;
    border-radius: 8px;
    transition: background 0.2s, transform 0.15s;
  }
  .coop-btn:hover {
    background: var(--accent-dark);
    transform: translateY(-2px);
  }

  /* =========================================================
     页面 4：近期项目（时间线）
     ========================================================= */
  .project-hero {
    padding: 80px 0 40px;
    text-align: center;
  }
  .project-hero h1 {
    font-size: 40px;
    font-weight: 800;
    color: var(--primary);
    margin-bottom: 12px;
  }
  .project-hero p {
    color: var(--text-light);
    font-size: 16px;
    max-width: 640px;
    margin: 0 auto;
  }

  .timeline {
    position: relative;
    padding: 40px 0 80px;
    max-width: 900px;
    margin: 0 auto;
  }
  .timeline::before {
    content: "";
    position: absolute;
    left: 24px; top: 40px; bottom: 40px;
    width: 2px;
    background: linear-gradient(to bottom, var(--primary), var(--accent));
    border-radius: 1px;
  }

  .timeline-item {
    position: relative;
    padding-left: 72px;
    margin-bottom: 32px;
  }
  .timeline-dot {
    position: absolute;
    left: 14px; top: 24px;
    width: 22px; height: 22px;
    background: #fff;
    border: 3px solid var(--primary);
    border-radius: 50%;
    box-shadow: 0 0 0 4px rgba(30, 58, 95, 0.08);
  }
  .timeline-item:first-child .timeline-dot {
    border-color: var(--accent);
    box-shadow: 0 0 0 4px rgba(232, 168, 56, 0.15);
  }

  .timeline-card {
    background: #fff;
    border-radius: 12px;
    padding: 24px 26px;
    border: 1px solid var(--border);
    transition: transform 0.2s, box-shadow 0.2s, border-color 0.2s;
  }
  .timeline-card:hover {
    transform: translateX(4px);
    box-shadow: 0 8px 24px rgba(30, 58, 95, 0.08);
    border-color: #cfd9e6;
  }
  .timeline-date {
    display: inline-block;
    font-size: 12px;
    font-weight: 700;
    color: var(--accent-dark);
    background: #fff4dd;
    padding: 2px 10px;
    border-radius: 10px;
    margin-bottom: 10px;
  }
  .timeline-card h3 {
    font-size: 18px;
    color: var(--primary);
    margin-bottom: 8px;
  }
  .timeline-card p {
    font-size: 14px;
    color: var(--text-light);
    line-height: 1.7;
  }

  /* =========================================================
     页面 5：往期活动
     ========================================================= */
  .section-title {
    text-align: center;
    font-size: 32px;
    font-weight: 800;
    color: var(--primary);
    margin: 60px 0 8px;
  }
  .section-subtitle {
    text-align: center;
    font-size: 14px;
    color: #888;
    margin-bottom: 32px;
  }

  .filter-bar {
    max-width: 1100px;
    margin: 0 auto 28px;
    display: flex;
    flex-wrap: wrap;
    gap: 12px 24px;
    align-items: center;
    justify-content: center;
  }
  .filter-group {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 8px;
  }
  .filter-label {
    font-size: 14px;
    font-weight: 600;
    color: #555;
    margin-right: 4px;
  }
  .tag-btn {
    padding: 6px 18px;
    border: 1.5px solid #d0d5dd;
    background: #fff;
    border-radius: 20px;
    font-size: 14px;
    color: #444;
    cursor: pointer;
    transition: all 0.2s;
    font-family: inherit;
  }
  .tag-btn:hover { border-color: var(--primary); color: var(--primary); }
  .tag-btn.active {
    background: var(--primary);
    border-color: var(--primary);
    color: #fff;
  }
  .year-select {
    padding: 7px 16px;
    border: 1.5px solid #d0d5dd;
    border-radius: 20px;
    font-size: 14px;
    color: #444;
    background: #fff;
    cursor: pointer;
    outline: none;
    font-family: inherit;
  }
  .year-select:focus { border-color: var(--primary); }

  .card-grid {
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 24px;
    padding-bottom: 80px;
  }

  .card {
    background: #fff;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 12px rgba(0, 0, 0, 0.07);
    transition: transform 0.2s, box-shadow 0.2s;
    display: flex;
    flex-direction: column;
  }
  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
  }

  .card-header { padding: 16px 18px 10px; }
  .card-label {
    display: inline-block;
    font-size: 12px;
    padding: 2px 10px;
    border-radius: 10px;
    background: #eef3fa;
    color: var(--primary);
    margin-bottom: 8px;
  }
  .card-title-text {
    font-size: 16px;
    font-weight: 600;
    color: var(--text);
    line-height: 1.5;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  .card-desc {
    font-size: 13px;
    color: #777;
    margin-top: 4px;
    line-height: 1.5;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }

  .card-cover {
    display: block;
    width: 100%;
    aspect-ratio: 16 / 9;
    overflow: hidden;
    background: #f0f0f0;
    position: relative;
  }
  .card-cover img {
    width: 100%; height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.3s;
  }
  .card-cover:hover img { transform: scale(1.04); }
  .cover-placeholder {
    width: 100%; height: 100%;
    display: flex; align-items: center; justify-content: center;
    color: #aaa; font-size: 14px;
    background: #f5f5f5;
  }

  .card-footer {
    padding: 12px 18px 16px;
    display: flex;
    gap: 20px;
    font-size: 13px;
    color: #888;
    margin-top: auto;
  }
  .card-footer span { display: flex; align-items: center; gap: 4px; }

  .empty-tip {
    grid-column: 1 / -1;
    text-align: center;
    padding: 60px 20px;
    color: #aaa;
    font-size: 15px;
  }

  /* 全局页脚 */
  .site-footer {
    text-align: center;
    padding: 30px 20px;
    color: #999;
    font-size: 13px;
    border-top: 1px solid var(--border);
    background: #fff;
  }
</style>
</head>
<body>

<!-- ============================================================
     顶部导航
     ============================================================ -->
<nav class="navbar">
  <a href="#home" class="nav-logo">多彩梦交通文化综合体</a>
  <div class="nav-menu">
    <a class="nav-link primary-link" data-page="home" href="#home">组织简介</a>
    <a class="nav-link primary-link" data-page="contact" href="#contact">联系我们</a>
    <a class="nav-link primary-link" data-page="coop" href="#coop">参与共创</a>

    <div class="hamburger-wrap" id="hamburgerWrap">
      <button class="hamburger-btn" id="hamburgerBtn" aria-label="更多菜单">
        <svg viewBox="0 0 24 24"><path d="M3 6h18M3 12h18M3 18h18"/></svg>
      </button>
      <div class="hamburger-dropdown" id="hamburgerDropdown">
        <a class="nav-link" data-page="project" href="#project">近期项目</a>
        <a class="nav-link" data-page="activities" href="#activities">往期活动</a>
      </div>
    </div>
  </div>
</nav>

<main>

  <!-- ============================================================
       页面 1：组织简介
       ============================================================ -->
  <section id="page-home" class="page active">
    <div class="home-hero">
      <div class="container">
        <span class="home-hero-tag">关于我们</span>
        <h1>多彩梦交通文化综合体</h1>
        <p>我们是一个交通爱好者团体，主要开展线下线上各类交通主题游戏和活动，精彩丰富，并致力于打造交通爱好者共建共享的开放平台。无论你是轨道迷、公交迷、航空迷还是公路迷，这里都有属于你的位置。</p>
      </div>
    </div>

    <div class="container">
      <div class="home-split">
        <div class="home-story">
          <h2>我们是谁</h2>
          <p>多彩梦交通文化综合体是一个由交通爱好者自发组成的开放团体，聚集了来自不同城市、不同年龄段、不同交通兴趣方向的朋友。</p>
          <p>我们相信，交通不只是出行工具，更是一种文化、一种热爱、一种连接人与人的方式。通过线上交流与线下聚会，我们让这份热爱变得更有温度和归属感。</p>
          <p>我们持续举办各类主题活动、游戏、展览与团拜会，也欢迎每一位愿意参与的爱好者，一起来共建、共享这个平台。</p>
        </div>
        <div class="home-split-right">
          <div class="stat-grid">
            <div class="stat-item">
              <div class="stat-num">2<span>大</span></div>
              <div class="stat-label">常年主题活动</div>
            </div>
            <div class="stat-item">
              <div class="stat-num">多<span>类</span></div>
              <div class="stat-label">线上线下活动</div>
            </div>
            <div class="stat-item">
              <div class="stat-num">开放<span></span></div>
              <div class="stat-label">共建共享平台</div>
            </div>
            <div class="stat-item">
              <div class="stat-num">全年<span></span></div>
              <div class="stat-label">持续开展活动</div>
            </div>
          </div>
        </div>
      </div>

      <!-- 两大常年活动 -->
      <div class="annual-section">
        <h2 class="annual-title">两大常年主题活动</h2>
        <p class="annual-subtitle">多彩梦交通文化综合体旗下目前设有两大常年主题活动，期待您的参与</p>

        <div class="annual-grid">
          <div class="annual-card">
            <span class="annual-tag">暑期档</span>
            <h3>交通夏日展</h3>
            <div class="annual-time">每年 7–8 月 · 暑假期间</div>
            <p>聚焦交通文化的夏日主题展览与互动活动，包含模型展示、主题游戏、爱好者交流等环节，是每年夏天交通迷们最期待的线下盛会。</p>
          </div>
          <div class="annual-card alt">
            <span class="annual-tag">新春档</span>
            <h3>新春交通团拜会</h3>
            <div class="annual-time">每年新春佳节期间</div>
            <p>在新春佳节与交通爱好者朋友们相聚一堂，畅聊热爱、分享收获、共迎新年，用交通人自己的方式开启崭新的一年。</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================================
       页面 2：联系我们
       ============================================================ -->
  <section id="page-contact" class="page">
    <div class="contact-hero container">
      <h1>联系我们</h1>
      <p>有任何想法、合作意向或问题，欢迎通过以下任一方式找到我们。我们通常会在 1–2 个工作日内回复。</p>
    </div>

    <div class="container">
      <div class="contact-grid">
        <div class="contact-card">
          <div class="contact-icon">💬</div>
          <h3>微信公众号</h3>
          <p>搜索「多彩梦交通文化综合体」</p>
        </div>
        <div class="contact-card">
          <div class="contact-icon">📧</div>
          <h3>邮箱</h3>
          <p>hello@duocaimeng.com</p>
        </div>
        <div class="contact-card">
          <div class="contact-icon">📺</div>
          <h3>B 站</h3>
          <p>@多彩梦交通文化综合体</p>
        </div>
        <div class="contact-card">
          <div class="contact-icon">📍</div>
          <h3>线下活动</h3>
          <p>详见活动公告</p>
        </div>
      </div>

      <div class="contact-cta">
        <a class="top-btn"
           href="https://metro-lingnandongdao.github.io/lingnan-portfolio/sites.html">
          找到我们
        </a>
      </div>
    </div>
  </section>

  <!-- ============================================================
       页面 3：参与共创
       ============================================================ -->
  <section id="page-coop" class="page">
    <div class="coop-hero">
      <div class="container">
        <h1>参与共创</h1>
        <p>我们是一个开放的平台，这里没有观众席，每一位交通爱好者都可以是组织者、创作者和参与者。</p>
      </div>
    </div>

    <div class="container">
      <div class="coop-steps">
        <div class="coop-step">
          <div class="coop-step-num">1</div>
          <h3>提出你的想法</h3>
          <p>无论是一场主题聚会、一个线上游戏、一次模型展示，还是一次线路体验，先告诉我们你想做什么。</p>
        </div>
        <div class="coop-step">
          <div class="coop-step-num">2</div>
          <h3>找到同好伙伴</h3>
          <p>我们会帮你匹配有相似兴趣的伙伴，一起把想法打磨成可执行的方案，让活动更有趣、更完整。</p>
        </div>
        <div class="coop-step">
          <div class="coop-step-num">3</div>
          <h3>一起落地实现</h3>
          <p>从策划、宣传到执行，我们提供力所能及的资源支持，把每一次共创真正做出来、办精彩。</p>
        </div>
      </div>

      <div class="coop-cta-wrap">
        <h2>准备好加入了吗？</h2>
        <p>把你的想法通过邮箱或公众号发给我们，开启你的交通共创之旅。</p>
        <a class="coop-btn" href="#contact">立即联系</a>
      </div>
    </div>
  </section>

  <!-- ============================================================
       页面 4：近期项目
       ============================================================ -->
  <section id="page-project" class="page">
    <div class="project-hero container">
      <h1>近期项目</h1>
      <p>正在筹备或刚刚完成的交通主题活动与共创项目，欢迎关注与参与。</p>
    </div>

    <div class="container">
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-card">
            <span class="timeline-date">2026 · 暑期</span>
            <h3>交通夏日展 · 2026</h3>
            <p>一年一度的暑期交通主题展，包含模型展示、互动游戏、线路分享与爱好者交流会，欢迎各位交通迷前来相聚。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-card">
            <span class="timeline-date">2026 · 新春</span>
            <h3>新春交通团拜会 · 2026</h3>
            <p>新春佳节期间与交通爱好者朋友们相聚一堂，分享过去一年的精彩瞬间，共同展望新一年的活动计划。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-card">
            <span class="timeline-date">2025 · 暑期</span>
            <h3>交通夏日展 · 2025</h3>
            <p>盛夏时节的交通主题展览与互动活动，吸引了众多交通爱好者参与，留下了许多精彩瞬间。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-card">
            <span class="timeline-date">2025 · 新春</span>
            <h3>新春交通团拜会 · 2025</h3>
            <p>春节期间举办的交通爱好者团拜活动，大家欢聚一堂，畅聊热爱，共贺新春。</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ============================================================
       页面 5：往期活动
       ============================================================ -->
  <section id="page-activities" class="page">
    <h2 class="section-title">往期活动</h2>
    <p class="section-subtitle">点击封面即可跳转观看</p>

    <div class="filter-bar">
      <div class="filter-group" id="tagFilterGroup">
        <span class="filter-label">分类：</span>
      </div>
      <div class="filter-group">
        <span class="filter-label">年份：</span>
        <select class="year-select" id="yearSelect">
          <option value="all">全部年份</option>
        </select>
      </div>
    </div>

    <div class="card-grid" id="cardGrid"></div>
  </section>

</main>

<footer class="site-footer">
  © 2026 多彩梦交通文化综合体 · 打造交通爱好者共建共享的开放平台
</footer>


<script>
/* ============================================================
   ★★★ 活动数据配置区 ★★★

   字段说明：
   - bvid       : B站视频 BV 号（必填），也支持粘贴完整视频链接
   - year       : 年份（必填），例如 "2025"
   - tags       : 标签数组（必填），例如 ["交通夏日展", "线下"]
   - customText : 卡片标题文字（选填）。不填自动读 B站标题
   - customDesc : 卡片简介文字（选填）。不填自动读 B站简介
   - label      : 卡片左上角小标签（选填）

   优先级：
   标题：customText → B站标题 → "未命名活动"
   简介：customDesc → B站简介 → 不显示
   ============================================================ */
const ACTIVITIES = [
  {
    bvid: "BV1558B6GEun",
    year: "2026",
    tags: ["交通夏日展", "网络展播"],
    customText: "2026全都暑于你下半场",
    customDesc: "2026第二届全都暑于你交通夏日展（下半场）——盛夏交通主题展播精彩回顾",
    label: "夏日展"
  },
  {
    bvid: "BV1N6bi6XE5Q",
    year: "2026",
    tags: ["交通夏日展", "网络展播"],
    customText: "2026全都暑于你上半场",
    customDesc: "2026第二届全都暑于你交通夏日展（上半场）——盛夏交通主题展播精彩回顾",
    label: "夏日展"
  },
  {
    bvid: "BV17NfGByEeY",
    year: "2026",
    tags: ["新春团拜会", "网络展播"],
    customText: "2026聚交生活马上出发正片下半场",
    customDesc: "2026聚交生活马上出发新春交通团拜会（正片下半场）——丙午马年新春交通主题展播精彩回顾",
    label: "新春纪"
  },
  {
    bvid: "BV1mqZ2BdEDM",
    year: "2026",
    tags: ["新春团拜会", "网络展播"],
    customText: "2026聚交生活马上出发正片上半场",
    customDesc: "2026聚交生活马上出发新春交通团拜会（正片上半场）——丙午马年新春交通主题展播精彩回顾",
    label: "新春纪"
  },
  {
    bvid: "BV1ByAzziEXA",
    year: "2026",
    tags: ["新春团拜会", "网络展播"],
    customText: "2026聚交生活马上出发预热场",
    customDesc: "2026聚交生活马上出发新春交通团拜会（预热场）——丙午马年新春交通主题展播精彩回顾",
    label: "新春纪"
  },
];


/* ============================================================
   一、路由 / 页面切换
   ============================================================ */
(function setupRouter() {
  const pages = ["home", "contact", "coop", "project", "activities"];

  function switchPage(name) {
    if (!pages.includes(name)) name = "home";
    document.querySelectorAll(".page").forEach(el => el.classList.remove("active"));
    const target = document.getElementById("page-" + name);
    if (target) target.classList.add("active");

    document.querySelectorAll(".nav-link").forEach(el => {
      el.classList.toggle("active", el.dataset.page === name);
    });

    const dd = document.getElementById("hamburgerDropdown");
    if (dd) dd.classList.remove("show");

    window.scrollTo({ top: 0, behavior: "instant" });
  }

  function handleHash() {
    const hash = (location.hash || "#home").replace("#", "");
    switchPage(hash);
  }

  window.addEventListener("hashchange", handleHash);
  handleHash();

  const btn = document.getElementById("hamburgerBtn");
  const dd = document.getElementById("hamburgerDropdown");
  if (btn && dd) {
    btn.addEventListener("click", (e) => {
      e.stopPropagation();
      dd.classList.toggle("show");
    });
    document.addEventListener("click", () => dd.classList.remove("show"));
    dd.addEventListener("click", (e) => e.stopPropagation());
  }
})();


/* ============================================================
   二、往期活动逻辑（含三重代理 + 数据校验）
   ============================================================ */

function extractBvid(input) {
  if (!input) return "";
  const s = String(input).trim();
  if (/^BV[0-9A-Za-z]+$/.test(s)) return s;
  const match = s.match(/BV[0-9A-Za-z]+/);
  return match ? match[0] : s;
}

function formatNumber(n) {
  if (n === undefined || n === null || isNaN(n)) return "—";
  if (n >= 100000000) return (n / 100000000).toFixed(1) + "亿";
  if (n >= 10000) return (n / 10000).toFixed(1) + "万";
  return String(n);
}

async function fetchBiliInfo(bvid) {
  if (!bvid) return null;
  const api = `https://api.bilibili.com/x/web-interface/view?bvid=${encodeURIComponent(bvid)}`;

  const attempts = [
    async () => {
      const r = await fetch(api, { referrerPolicy: "no-referrer" });
      if (!r.ok) throw new Error("直连失败 " + r.status);
      return await r.json();
    },
    async () => {
      const r = await fetch("https://api.allorigins.win/raw?url=" + encodeURIComponent(api));
      if (!r.ok) throw new Error("allorigins 失败 " + r.status);
      return await r.json();
    },
    async () => {
      const r = await fetch("https://api.codetabs.com/v1/proxy?quest=" + encodeURIComponent(api));
      if (!r.ok) throw new Error("codetabs 失败 " + r.status);
      return await r.json();
    }
  ];

  for (let i = 0; i < attempts.length; i++) {
    try {
      const json = await attempts[i]();
      if (json && json.code === 0 && json.data) {
        const d = json.data;
        return {
          title: d.title || "",
          desc: d.desc || "",
          pic: d.pic || "",
          views: d.stat ? d.stat.view : null,
          likes: d.stat ? d.stat.like : null,
          link: `https://www.bilibili.com/video/${bvid}`
        };
      }
    } catch (e) {
      console.warn("[往期活动] 通道 " + (i + 1) + " 失败:", e.message);
    }
  }
  console.warn("[往期活动] 所有通道均失败，BV号:", bvid);
  return null;
}

let allCards = [];
let currentTag = "all";
let currentYear = "all";

function renderCards() {
  const grid = document.getElementById("cardGrid");
  if (!grid) return;

  const filtered = allCards.filter(card => {
    const tagOk = currentTag === "all" || (card.tags || []).includes(currentTag);
    const yearOk = currentYear === "all" || card.year === currentYear;
    return tagOk && yearOk;
  });

  if (filtered.length === 0) {
    grid.innerHTML = `<div class="empty-tip">暂无符合条件的活动</div>`;
    return;
  }

  grid.innerHTML = filtered.map(card => {
    const info = card.info || {};

    const titleText = card.customText || info.title || "未命名活动";
    const descText  = card.customDesc || info.desc  || "";

    const coverHtml = info.pic
      ? `<a class="card-cover" href="${info.link}" target="_blank" rel="noopener noreferrer">
           <img src="${info.pic}" alt="${titleText}"
                referrerpolicy="no-referrer" loading="lazy">
         </a>`
      : `<div class="card-cover"><div class="cover-placeholder">封面加载中…</div></div>`;

    return `
      <div class="card">
        <div class="card-header">
          ${card.label ? `<span class="card-label">${card.label}</span>` : ""}
          <div class="card-title-text">${titleText}</div>
          ${descText ? `<div class="card-desc">${descText}</div>` : ""}
        </div>
        ${coverHtml}
        <div class="card-footer">
          <span>▶ ${formatNumber(info.views)}</span>
          <span>👍 ${formatNumber(info.likes)}</span>
        </div>
      </div>
    `;
  }).join("");
}

function renderTagFilter() {
  const group = document.getElementById("tagFilterGroup");
  if (!group) return;

  const allTags = new Set();
  allCards.forEach(card => {
    (card.tags || []).forEach(t => allTags.add(t));
  });

  group.innerHTML = '<span class="filter-label">分类：</span>';

  const allBtn = document.createElement("button");
  allBtn.className = "tag-btn" + (currentTag === "all" ? " active" : "");
  allBtn.textContent = "全部";
  allBtn.onclick = () => { currentTag = "all"; renderTagFilter(); renderCards(); };
  group.appendChild(allBtn);

  [...allTags].sort().forEach(tag => {
    const btn = document.createElement("button");
    btn.className = "tag-btn" + (currentTag === tag ? " active" : "");
    btn.textContent = tag;
    btn.onclick = () => { currentTag = tag; renderTagFilter(); renderCards(); };
    group.appendChild(btn);
  });
}

function renderYearFilter() {
  const sel = document.getElementById("yearSelect");
  if (!sel) return;

  const years = [...new Set(allCards.map(c => c.year).filter(Boolean))].sort().reverse();
  sel.innerHTML = '<option value="all">全部年份</option>';
  years.forEach(y => {
    const opt = document.createElement("option");
    opt.value = y;
    opt.textContent = y + " 年";
    if (currentYear === y) opt.selected = true;
    sel.appendChild(opt);
  });
  sel.onchange = () => { currentYear = sel.value; renderCards(); };
}

async function initActivities() {
  const grid = document.getElementById("cardGrid");
  if (!grid) return;

  try {
    if (!Array.isArray(ACTIVITIES)) {
      throw new Error("ACTIVITIES 不是一个数组，请检查语法");
    }

    allCards = ACTIVITIES.map(item => {
      if (!item || typeof item !== "object") {
        console.warn("[往期活动] 跳过非对象项:", item);
        return null;
      }
      const bvid = extractBvid(item.bvid);
      if (!bvid || !/^BV/.test(bvid)) {
        console.warn("[往期活动] 跳过无效 bvid:", item);
        return null;
      }
      return {
        ...item,
        bvid,
        tags: Array.isArray(item.tags) ? item.tags : [],
        info: null
      };
    }).filter(Boolean);

    renderTagFilter();
    renderYearFilter();
    renderCards();

    await Promise.all(allCards.map(async (card) => {
      try {
        card.info = await fetchBiliInfo(card.bvid);
      } catch (e) {
        console.warn("[往期活动] 拉取失败:", card.bvid, e);
      }
    }));

    renderCards();

  } catch (err) {
    console.error("[往期活动] 初始化失败:", err);
    grid.innerHTML =
      `<div class="empty-tip">
         ⚠️ 数据加载出错：${err.message}<br>
         <span style="font-size:12px;color:#bbb;">
           请检查 const ACTIVITIES 的语法（逗号、引号、括号）
         </span>
       </div>`;
  }
}

initActivities();
</script>

</body>
</html>
