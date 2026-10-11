# dotsmileTCU.github.io

多彩梦交通文化综合体旗下目前有交通夏日展和新春交通团拜会两个子品牌。致力于交通爱好者共建共享的文化分享平台。

<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>往期活动 - 岭南道</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC",
                 "Microsoft YaHei", sans-serif;
    background: #f7f8fa;
    color: #1a1a2e;
    padding: 20px;
  }

  /* ===== 第一部分：顶部按钮 ===== */
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

  /* ===== 第二部分：往期活动 ===== */
  .section-title {
    text-align: center;
    font-size: 26px;
    font-weight: 700;
    color: #1e3a5f;
    margin-bottom: 8px;
  }
  .section-subtitle {
    text-align: center;
    font-size: 14px;
    color: #888;
    margin-bottom: 28px;
  }

  /* --- 筛选栏 --- */
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
  }
  .tag-btn:hover {
    border-color: #1e3a5f;
    color: #1e3a5f;
  }
  .tag-btn.active {
    background: #1e3a5f;
    border-color: #1e3a5f;
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
  }
  .year-select:focus {
    border-color: #1e3a5f;
  }

  /* --- 卡片网格 --- */
  .card-grid {
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 24px;
    padding-bottom: 60px;
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

  /* 卡片上部：自定义文字 */
  .card-header {
    padding: 16px 18px 10px;
  }
  .card-label {
    display: inline-block;
    font-size: 12px;
    padding: 2px 10px;
    border-radius: 10px;
    background: #eef3fa;
    color: #1e3a5f;
    margin-bottom: 8px;
  }
  .card-title-text {
    font-size: 16px;
    font-weight: 600;
    color: #1a1a2e;
    line-height: 1.5;
  }
  .card-desc {
    font-size: 13px;
    color: #777;
    margin-top: 4px;
    line-height: 1.5;
  }

  /* 卡片中部：封面 */
  .card-cover {
    display: block;
    width: 100%;
    aspect-ratio: 16 / 9;
    overflow: hidden;
    background: #f0f0f0;
    position: relative;
  }
  .card-cover img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.3s;
  }
  .card-cover:hover img {
    transform: scale(1.04);
  }
  .cover-placeholder {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #aaa;
    font-size: 14px;
    background: #f5f5f5;
  }

  /* 卡片下部：视频数据 */
  .card-footer {
    padding: 12px 18px 16px;
    display: flex;
    gap: 20px;
    font-size: 13px;
    color: #888;
    margin-top: auto;
  }
  .card-footer span {
    display: flex;
    align-items: center;
    gap: 4px;
  }
  .card-footer .icon {
    font-size: 14px;
  }

  /* 空状态 */
  .empty-tip {
    grid-column: 1 / -1;
    text-align: center;
    padding: 60px 20px;
    color: #aaa;
    font-size: 15px;
  }
</style>
</head>
<body>

<!-- ============================================================
     第一部分：顶部按钮 —— “找到我们”
     ============================================================ -->
<div class="top-btn-wrap">
  <a class="top-btn" href="https://metro-lingnandongdao.github.io/lingnan-portfolio/sites.html">
    找到我们
  </a>
</div>


<!-- ============================================================
     第二部分：往期活动
     ============================================================ -->
<h2 class="section-title">往期活动</h2>
<p class="section-subtitle">点击封面即可跳转观看</p>

<!-- 筛选栏 -->
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

<!-- 卡片容器 -->
<div class="card-grid" id="cardGrid"></div>


<script>
/* ============================================================
   ★★★ 活动数据配置区 ★★★
   在这里添加你的活动卡片。每一条对应一张卡片。

   字段说明：
   - bvid       : B站视频的 BV 号（必填），例如 "BV1xx411c7mD"
                  也可以直接粘贴完整视频链接，程序会自动提取 BV 号
   - year       : 年份（必填），例如 "2025"
   - tags       : 标签数组（必填），例如 ["年会", "线下"]
   - customText : 卡片上部自定义展示的文字（必填）
   - customDesc : 卡片上部自定义描述文字（选填）
   - label      : 卡片左上角小标签（选填）

   添加方法：复制下面 { ... } 整块，改字段值即可。
   ============================================================ */
const ACTIVITIES = [
  {
    bvid: "BV1xx411c7mD",
    year: "2025",
    tags: ["年会", "线下"],
    customText: "2025 年度见面会",
    customDesc: "岭南道年度线下聚会，精彩回顾",
    label: "年度活动"
  },
  {
    bvid: "BV1yy411c7mD",
    year: "2025",
    tags: ["工作坊", "线上"],
    customText: "新媒体运营工作坊",
    customDesc: "从 0 到 1 搭建个人品牌",
    label: "工作坊"
  },
  {
    bvid: "BV1zz411c7mD",
    year: "2024",
    tags: ["年会"],
    customText: "2024 年度总结大会",
    customDesc: "回顾过去一年的成长",
    label: "年度活动"
  }
  // ★ 继续在这里添加更多活动……
];


/* ============================================================
   以下为自动逻辑，一般不需要修改
   ============================================================ */

// --- 从输入中提取 BV 号（支持纯 BV 号或完整 URL）---
function extractBvid(input) {
  if (!input) return "";
  if (/^BV[0-9A-Za-z]+$/.test(input.trim())) return input.trim();
  const match = input.match(/BV[0-9A-Za-z]+/);
  return match ? match[0] : input.trim();
}

// --- 数字格式化（万 / 亿）---
function formatNumber(n) {
  if (n === undefined || n === null) return "—";
  if (n >= 100000000) return (n / 100000000).toFixed(1) + "亿";
  if (n >= 10000) return (n / 10000).toFixed(1) + "万";
  return String(n);
}

// --- 从 B站 API 获取视频信息（游客态即可）---
async function fetchBiliInfo(bvid) {
  const url = `https://api.bilibili.com/x/web-interface/view?bvid=${bvid}`;
  try {
    const res = await fetch(url);
    const json = await res.json();
    if (json.code === 0 && json.data) {
      const d = json.data;
      return {
        title: d.title || "",
        pic: d.pic || "",
        views: d.stat ? d.stat.view : null,
        likes: d.stat ? d.stat.like : null,
        link: `https://www.bilibili.com/video/${bvid}`
      };
    }
    return null;
  } catch (e) {
    console.warn("获取 B站视频信息失败:", bvid, e);
    return null;
  }
}

// --- 全局状态 ---
let allCards = [];
let currentTag = "all";
let currentYear = "all";

// --- 渲染卡片 ---
function renderCards() {
  const grid = document.getElementById("cardGrid");
  const filtered = allCards.filter(card => {
    const tagOk = currentTag === "all" || card.tags.includes(currentTag);
    const yearOk = currentYear === "all" || card.year === currentYear;
    return tagOk && yearOk;
  });

  if (filtered.length === 0) {
    grid.innerHTML = `<div class="empty-tip">暂无符合条件的活动</div>`;
    return;
  }

  grid.innerHTML = filtered.map(card => {
    const info = card.info || {};
    const coverHtml = info.pic
      ? `<a class="card-cover" href="${info.link}" target="_blank" rel="noopener noreferrer">
           <img src="${info.pic}" alt="${info.title || '视频封面'}"
                referrerpolicy="no-referrer" loading="lazy">
         </a>`
      : `<div class="card-cover"><div class="cover-placeholder">封面加载中…</div></div>`;

    return `
      <div class="card">
        <div class="card-header">
          ${card.label ? `<span class="card-label">${card.label}</span>` : ""}
          <div class="card-title-text">${card.customText || info.title || "未命名活动"}</div>
          ${card.customDesc ? `<div class="card-desc">${card.customDesc}</div>` : ""}
        </div>
        ${coverHtml}
        <div class="card-footer">
          <span><span class="icon">▶</span> ${formatNumber(info.views)}</span>
          <span><span class="icon">👍</span> ${formatNumber(info.likes)}</span>
        </div>
      </div>
    `;
  }).join("");
}

// --- 渲染标签筛选按钮 ---
function renderTagFilter() {
  const allTags = new Set();
  allCards.forEach(card => {
    (card.tags || []).forEach(t => allTags.add(t));
  });

  const group = document.getElementById("tagFilterGroup");
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

// --- 渲染年份下拉 ---
function renderYearFilter() {
  const years = [...new Set(allCards.map(c => c.year).filter(Boolean))].sort().reverse();
  const sel = document.getElementById("yearSelect");
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

// --- 初始化 ---
async function init() {
  allCards = ACTIVITIES.map(item => ({ ...item, info: null }));

  renderTagFilter();
  renderYearFilter();

  await Promise.all(
    allCards.map(async (card) => {
      const bvid = extractBvid(card.bvid);
      card.info = await fetchBiliInfo(bvid);
    })
  );

  renderCards();
}

init();
</script>

</body>
</html>
