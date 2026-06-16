# personal-site 任务源

> **当前阶段**：v1.2 视觉设计升级 — ISS-017~022 全部落地，build 通过。下一步：本地预览确认 + 提交。

## 活跃任务

- **ISS-017** 色彩体系升级 [P0] ✅ — 替换 CSS 变量，从暖灰+棕升级为「律政金」色系（古金、深铜、羊皮纸白 + 墨绿/法袍绿对比色），全站通过 CSS 变量一键生效
  - 改动范围：`site.css` 变量声明
  - 色板：`#faf8f5` / `#f5f0e8` / `#c4a882` / `#8b6f47` / `#5a3e28` / `#1a2332` / `#2d4a3e` / `#4a7c59`

- **ISS-018** Hero 区域重设计 [P0] ✅ — 加入大型装饰性法律符号（§ / ¶）作背景纹理，金色渐变分隔线，更考究的间距与排版节奏
  - 改动范围：`HomePage.astro` + `site.css` `.hero` 相关样式

- **ISS-019** 产品卡片重设计 [P1] ✅ — 改为纵向布局（图标在上，文字在下），图标加渐变底色，卡片顶部用细线渐变条代替粗边框，增加留白
  - 改动范围：`ProductCard.astro` + `site.css` `.product-card` 相关样式

- **ISS-020** 字体加载优化 [P1] ✅ — 引入 Inter（英文）+ Noto Sans SC（中文）+ JetBrains Mono + Noto Serif SC 替代系统字体，提升排版品质
  - 改动范围：`BaseLayout.astro` 加载 Google Fonts，`site.css` 字体变量

- **ISS-021** 滚动动效 [P2] ✅ — 用 Intersection Observer 实现 scroll-reveal（fade-up），导航栏滚动时的微妙阴影变化，所有动效 ≤300ms，克制精致
  - 改动范围：`site.css` 动画定义 + `BaseLayout.astro` 内联 `<script>`

- **ISS-022** 详情页视觉一致性 [P2] ✅ — 统一产品详情页 Hero 风格，每个产品用独立色彩主题装饰符号（Folia:¶ sage / FaroPDF:§ steel / LegalSkills:∴ royal / AgentExecutor:λ amber）
  - 改动范围：`FoliaPage.astro` / `FaroPdfPage.astro` / `LegalSkillsPage.astro` / `AgentExecutorPage.astro` + `site.css`

- **ISS-015** Agent Execute Recast 插件集成 — 在主页新增第 4 张产品卡 + 详情页（与 Folia / FaroPDF / Legal Skills 同级）

- **ISS-016** ~~产品页功能卡 hover 动画统一~~ ✅ — 以 LegalSkillsPage `.skill-card` 为基准，为 FoliaPage / FaroPdfPage / AgentExecutorPage 的 `.feature-card` 补齐一致的 hover 交互（translateY(-4px) scale(1.012) + shadow + border-top 3→5px + focus-visible）；首页 ProductCard 保持更轻力度（translateY(-2px) / 160ms）

### 远期候选

- v1.1：i18n 同步到产品仓 README / blog 子栏目
- v1.2：analytics（Umani / Plausible）/ SEO（sitemap + meta + OG）/ 自定义域（已取消，可重启）

### 跨仓遗留

- Folia README 官网链接仍指向旧 URL `/personal-site/folia/` → 应改为 `/folia/`
- FaroPDF README download 部分仍说"待发布" → 应更新为 v0.1.1 已发布

## 已取消

- **ISS-008 自定义域**（2026-06-05 用户决策取消，保持 `cat-xierluo.github.io/`）

## 归档任务索引

详细实现记录见 CHANGELOG.md；决策背景见 docs/DECISIONS.md。

| ISS | 标题 | 日期 | 交付物 |
| --- | --- | --- | --- |
| ISS-001 | scaffold + bio + 产品列表 | 2026-06-05 | commit `a92dacd`，3 页 5 段式 |
| ISS-002 | GitHub Pages workflow | 2026-06-05 | commit `01c4f75`，ISS-009 修复激活 |
| ISS-003 | Folia website 迁出 | 2026-06-05 | commit `3891da4`，5 段式详情页 |
| ISS-004 | FaroPDF 详情页扩全结构 | 2026-06-05 | commit `6d8f52b`，8 features |
| ISS-005 | 跨仓 cleanup | 2026-06-05 | PR-A + PR-B 已合并 |
| ISS-006 | 中英文切换 | 2026-06-05 | 自建 i18n 字典，6→6 页 |
| ISS-007 | 微信二维码 | 2026-06-05 | WechatQr 组件 + footer/contact QR |
| ISS-009 | 部署修复 | 2026-06-05 | PR #3，lock file + Node 22 + Pages 启用 |
| ISS-010 | 真实 QR 替换 | 2026-06-05 | 184KB 真图替换 1×1 占位 |
| ISS-011 | URL 去 subpath | 2026-06-05 | PR #6，仓名 → `cat-xierluo.github.io` |
| ISS-012 | Legal Skills 集成 | 2026-06-06 | PR #7，第 3 张产品卡 + 5 段式详情页 |
| ISS-013 | 48 skill 卡片 | 2026-06-06 | PR #9，4 大类分组 + hover + mono repo |
| ISS-014 | Header / Footer 简化 | 2026-06-07 | PR #10，净删 110 行 |
| ISS-017 | 色彩体系升级 | 2026-06-16 | site.css 全站变量替换 + 详情页 oklch 清理 |
| ISS-018 | Hero 区域重设计 | 2026-06-16 | § 装饰符号 + 金色分隔线 + 排版节奏 |
| ISS-019 | 产品卡片重设计 | 2026-06-16 | 纵向布局 + 渐变图标底色 + 渐变顶条 |
| ISS-020 | 字体加载优化 | 2026-06-16 | Google Fonts: Inter + Noto Sans/Serif SC + JetBrains Mono |
| ISS-021 | 滚动动效 | 2026-06-16 | IntersectionObserver reveal + nav scroll shadow |
| ISS-022 | 详情页视觉一致性 | 2026-06-16 | 4 产品页各配独立装饰符号 + 统一 Hero 间距 |

## 进度日志

- 2026-06-16：ISS-017~022 全部落地（v1.2 视觉设计升级六项任务，build 10 pages 通过）
- 2026-06-16：ISS-017~022 创建（v1.2 视觉设计升级六项任务）
- 2026-06-05：ISS-001~005 + ISS-006~007 + ISS-009~011（10 个任务，scaffold → 部署 → i18n → QR → URL）
- 2026-06-06：ISS-012~013 + 代码质量清理（Legal Skills 集成 + 48 skill 卡片）
- 2026-06-07：ISS-014 + v1.0 内容事实核查（Header/Footer 简化 + FaroPDF v0.1.1 同步）
