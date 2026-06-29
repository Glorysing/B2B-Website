# B2B 化妆品企业网站

**两个生产级 B2B 企业网站，完全手写 WordPress 主题，零页面构建器。**

<div align="center">

[![JSY 在线](https://img.shields.io/website?url=https%3A%2F%2Fjsybiotech.com&label=jsybiotech.com&up_message=在线&down_message=离线&color=267A6D)](https://jsybiotech.com)
[![南彤在线](https://img.shields.io/website?url=https%3A%2F%2Fnantong-plastic.com&label=nantong-plastic.com&up_message=在线&down_message=离线&color=1A5A8A)](https://nantong-plastic.com)
[![WordPress](https://img.shields.io/badge/CMS-WordPress_6.9+-21759B?logo=wordpress&logoColor=white)](https://wordpress.org)
[![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?logo=php&logoColor=white)](https://php.net)
[![双语](https://img.shields.io/badge/双语-中文_%2F_英文-4caf50)](https://jsybiotech.com)
[![Vibe Coding](https://img.shields.io/badge/Built_with-Vibe_Coding-FF6B35?logo=anthropic&logoColor=white)](https://www.anthropic.com)

</div>

---

面向两家中国 B2B 化妆品制造商的独立企业网站，各自基于完全手写的 WordPress 主题开发，覆盖中英双语产品展示、面向 20+ 出口市场的国际 SEO，以及在线询盘转化流程。

本项目采用 **Vibe Coding** 开发模式——以 Claude AI 作为协同编程伙伴，从零构建完整功能的生产级网站，大幅提升开发效率与代码质量。

---

## 项目概览

|  | [金圣业集团](https://jsybiotech.com) | [南彤科技](https://nantong-plastic.com) |
|:---|:---|:---|
| **公司全称** | 广州金圣业生物科技有限公司 | 广东南彤科技有限公司 |
| **业务方向** | 化妆品 OEM / ODM 灌装代工 | 化妆品泵头分装包装制造 |
| **主题名称** | `jsy-biotech` | `pump-nantong` |
| **SEO 方案** | 完全自建 `inc/seo.php` | AIOSEO + 自定义 hreflang 层 |
| **产品系统** | 自定义文章类型（`jsy_product`） | 119+ SKU，含完整规格字段 |
| **部署方式** | SSH 直连逐文件上传 | GitHub Actions → SFTP 自动部署 |
| **多语言** | EN / ZH（Polylang 目录模式） | EN / ZH（Polylang 目录模式） |
| **认证** | GMPC · ISO · FDA | ISO · SGS |

---

## 金圣业集团 · [jsybiotech.com](https://jsybiotech.com)

<div align="center">

[![JSY](https://img.shields.io/badge/JSY_ENTERPRISE-jsybiotech.com-267A6D?style=for-the-badge)](https://jsybiotech.com)

</div>

广州金圣业生物科技有限公司——广州本地化妆品 OEM/ODM 灌装代工厂，面向海外品牌客户。网站定位为**服务即产品**的 B2B 展示站：没有产品 SKU 目录，以五大配方品类和核心能力驱动询盘转化。

### 公司数据

| | |
|:---|:---|
| 行业经验 | 15+ 年 |
| 厂房面积 | 10,800+ ㎡ |
| 标准生产线 | 8 条 |
| 成熟配方 | 2,000+ 项 |
| 合作品牌 | 1,000+ 家 |
| 认证体系 | GMPC · ISO · FDA |
| 原料供应商 | Dow · Givaudan · BASF · CRODA |

### 产品品类

```
化妆品 OEM / ODM
├── 面部护肤    精华液、保湿霜、眼霜、面膜
├── 个人护理    身体乳、沐浴露、洁面、止汗
├── 彩妆        粉底、口红、眼妆
├── 洗护发品    洗发水、护发素、发膜
└── 精油香氛    精油、香氛、香薰
```

### 功能特性

| 功能 | 说明 |
|:---|:---|
| **视频轮播 Hero** | 全屏 3 张幻灯片，背景视频循环播放 + 文字覆盖层；幻灯内容可在 WP 设置面板中编辑 |
| **自定义产品 CPT** | `jsy_product` 文章类型 + `jsy_series` 分类法（5 个品类 slug：facial / personal / color / hair / aroma） |
| **产品粘性过滤器** | 产品页左侧 sticky 品类导航 + 数量徽章；JS 过滤 + URL hash 同步 |
| **完全自建 SEO 引擎** | `inc/seo.php` 接管全站 11 个页面——title、description、canonical、hreflang、OG、Twitter Card、JSON-LD |
| **浏览器语言自动跳转** | `navigator.language` 检测 → 自动跳转中文或英文，30 天 cookie 记录用户选择 |
| **双语翻译系统** | 自定义 `languages/translations.php` 查找表；`jsy_t()` / `jsy_et()` 辅助函数，无 gettext 开销 |
| **品牌 & 原料商滚动条** | 18 家合作品牌 logo + 16 家原料供应商 logo 无缝循环动画 |
| **结构化数据** | Organization（全站）· FAQPage（/faq/）· HowTo（/process/）· ContactPage（/contact/） |
| **WP 设置面板** | 自定义设置页面，可更新 Hero 幻灯内容、统计数字等可编辑文案，无需触碰代码 |

### 设计系统

| 变量名 | 色值 | 用途 |
|:---|:---|:---|
| Primary | `#267A6D` | 按钮、链接、图标（JSY Logo 实际颜色） |
| Deep | `#1A5548` | 子页面 Hero 背景 |
| Hover | `#3AA697` | 交互悬停态 |
| Gold Accent | `#B8965A` | Eyebrow 线条、装饰性点缀 |
| Background | `#FAFAF8` | 页面主背景（暖白米色） |
| Alt BG | `#F5F0E8` | 交替 section 背景 |
| 英文标题字体 | Cormorant Garamond 300 | 编辑风格衬线体 |
| 英文正文字体 | DM Sans | 正文阅读 |
| 中文字体 | Noto Serif SC / Noto Sans SC | 中文标题 / 正文 |

### 页面地图

| 路径 | 页面 | Schema |
|:---|:---|:---|
| `/` · `/en/` | 首页——视频 Hero / 数据带 / 服务 Tabs / 品类 / 工厂 / 认证 / 品牌滚动 | Organization |
| `/about/` | 关于我们——历史、企业文化、研发实力 | Organization |
| `/services/` | OEM / ODM / 来样定制 / 半成品供应 | — |
| `/products/` | 产品中心——5 大品类，左侧粘性过滤器 | — |
| `/process/` | 合作流程——分步骤详解 | HowTo |
| `/quality/` | 品控中心——检测流程 + 实验室 | — |
| `/certifications/` | 资质认证——GMPC · ISO · FDA · NMPA | — |
| `/cases/` | 合作案例 | — |
| `/faq/` | 常见问题 | FAQPage |
| `/contact/` | 询盘表单——核心转化页 | ContactPage |
| `/news/` | 行业动态 | — |

### 技术栈

| 层级 | 技术 |
|:---|:---|
| CMS | WordPress 6.9+ |
| 主题 | 手写 PHP（`jsy-biotech`），零页面构建器依赖 |
| 路由 | `inc/router.php`——`template_redirect` priority 1（在 Polylang canonical 之前触发） |
| 多语言 | Polylang 目录模式；`jsy_lang()` · `jsy_url()` · `jsy_t()` 辅助函数 |
| 前端 | 原生 HTML5 · CSS3 自定义属性 · 原生 JS |
| 字体 | Cormorant Garamond · DM Sans · Noto Serif/Sans SC |
| SEO | 完全自建 `inc/seo.php`，在所有主题控制页面上抑制 AIOSEO |
| 服务器 | LiteSpeed 缓存 + Cloudflare WAF |
| 部署 | SSH 逐文件上传 + `wc -c` 大小验证 |

---

## 南彤科技 · [nantong-plastic.com](https://nantong-plastic.com)

<div align="center">

[![南彤](https://img.shields.io/badge/南彤科技-nantong--plastic.com-1A5A8A?style=for-the-badge)](https://nantong-plastic.com)
[![Deploy](https://img.shields.io/badge/部署-GitHub_Actions-2088FF?logo=github-actions&logoColor=white)](https://github.com/features/actions)

</div>

广东南彤科技有限公司——2010 年成立的精密化妆品泵头生产商，服务全球 20+ 个出口市场，包括北美、欧洲、中东、东南亚、日韩。

### 公司数据

| | |
|:---|:---|
| 成立时间 | 2010 年 |
| 行业经验 | 15+ 年 |
| 注塑机台 | 80+ 台 |
| 厂房面积 | 10,000+ ㎡ |
| 月产能 | 2,000 万+ 个 |
| 出口市场 | 20+ 个国家 |
| 主要客户 | 宝洁 · 联合利华 · 花王 · 立白 · 自然堂 |

### 产品线

```
化妆品泵头包装
├── 泡沫泵系列    38/410 · 43/410 牙口，0.4–2cc 出液量
├── 乳液泵系列    精密计量出液，适用乳液 / 洗发水 / 身体护理
└── 真空泵瓶系列  30ml / 50ml / 75ml，隔氧无菌出液
```

### 功能特性

| 功能 | 说明 |
|:---|:---|
| **产品数据库** | 119+ SKU，含牙口规格、出液量、材质、MOQ、交期 |
| **智能询盘表单** | 从产品页打开时自动填充产品名称和规格；支持上传最多 10 个附件 |
| **产品详情页** | 服务端渲染，虚拟路由 `/products/{sku}/`，无需每款产品建 WP 页面 |
| **全球市场地图** | 可视化展示 20+ 出口国家 |
| **客户品牌墙** | 宝洁、联合利华、花王等国际知名品牌背书 |
| **认证展示页** | ISO、SGS、专利证书 |
| **行业资讯** | 公司动态与行业洞察 |
| **中英双语** | 完整翻译表；`ntp_t()` / `ntp_et()` 辅助函数 |

### 页面地图

| 路径 | 页面 |
|:---|:---|
| `/` · `/en/` | 首页 |
| `/products/` | 完整产品目录 |
| `/products/foam-pumps/` | 泡沫泵品类 |
| `/products/lotion-pumps/` | 乳液泵品类 |
| `/products/cosmetic-packaging/` | 化妆品包装品类 |
| `/products/{sku}/` | 产品详情页（虚拟路由） |
| `/about/` | 关于我们 |
| `/service/` · `/custom-service/` | 标准 / 定制服务 |
| `/quality-control/` | 品控流程 |
| `/certifications/` | 认证资质 |
| `/contact/` | 联系我们 / 询价表单 |
| `/news/` | 行业资讯 |
| `/stores/` | 阿里巴巴 · 中国制造网 店铺 |

### 技术栈

| 层级 | 技术 |
|:---|:---|
| CMS | WordPress 6.9+ |
| 主题 | 手写 PHP（`pump-nantong`），零页面构建器依赖 |
| 路由 | `inc/router.php`——`template_redirect` priority 1 |
| 多语言 | Polylang 目录模式；`ntp_lang()` · `ntp_url()` · `ntp_t()` 辅助函数 |
| 前端 | 原生 HTML5 · CSS3 · 原生 JS |
| 字体 | Google Fonts: Inter · Syne |
| SEO | AIOSEO（后台配置静态页）+ 自定义 `inc/seo.php`（虚拟路由产品 / 资讯页） |
| 服务器 | LiteSpeed 缓存 + Cloudflare WAF |
| 部署 | GitHub Actions → SFTP（checksum 对比，只上传有变更的文件） |

---

## 共同架构

两个主题独立开发，但遵循完全一致的架构约定。

```
theme/
├── functions.php            核心：翻译辅助函数、CPT 注册、资源加载、设置面板
├── header.php               响应式双语导航——滚动感知吸顶头部
├── footer.php               页脚：联系方式、社媒、语言切换器
├── front-page.php           首页模板
├── inc/
│   ├── router.php           虚拟 URL 路由（priority 1——在 Polylang canonical 之前触发）
│   ├── components.php       共享 UI 组件：页面 banner、询盘表单、CTA 条
│   ├── seo.php              SEO 引擎：hreflang、canonical、OG、JSON-LD
│   └── data.php             静态数据数组（FAQ 等）
├── page-templates/          各路由模板文件（由 router.php include）
│   ├── products.php
│   ├── product-detail.php
│   ├── category.php
│   ├── about.php
│   ├── service.php  ·  custom-service.php
│   ├── contact.php
│   ├── quality-control.php
│   ├── certifications.php
│   ├── news.php  ·  news-detail.php
│   └── faq.php（仅 JSY）
├── languages/
│   └── translations.php     双语查找表（中英文 key-value 对照）
└── assets/
    ├── css/main.css         单一样式表，CSS 自定义属性
    └── js/main.js           单一脚本文件
```

### 关键工程模式

**虚拟路由** — 两个主题均在 `template_redirect`（priority 1，早于 Polylang canonical redirect 的 priority 2）拦截 WordPress 模板解析，将 `/products/foam-pumps/` 和 `/news/{slug}/` 等 URL 指向 `page-templates/` 下的模板文件，无需为每个 URL 创建 WP 页面记录。拦截后手动设置 `$wp_query->is_404 = false; $wp_query->is_page = true;`，确保标题和 body class 渲染正常。

**LiteSpeed JS Defer 绕过** — LiteSpeed 会将所有 enqueue 的脚本改为 `type="litespeed/javascript"`，延迟到用户首次交互后才执行。凡是需要在首次交互前就绑定的事件监听器（滚动感知头部、自动初始化），均使用 `data-no-optimize="1"` 内联脚本，在 `wp_footer` priority 1 注入，完全绕过 LiteSpeed 合并器。

**无 gettext 双语方案** — 翻译由自定义 `translations.php` 查找表和类型化辅助函数（`jsy_t()` / `ntp_t()`）处理，跳过 `.po`/`.mo` 编译，同时覆盖网站的每一处文案。

**SEO 无插件锁定** — JSY 的 `inc/seo.php` 对全站 11 个页面拥有完全控制权：在所有主题管理的路由上抑制 AIOSEO，并从单一函数输出 title、description、canonical、hreflang、OG、Twitter Card 和 JSON-LD。南彤对静态 WP 页面使用 AIOSEO 后台配置，但在虚拟产品页和资讯页上复用相同的自定义 SEO 层。

---

### 关于 Vibe Coding

本项目完全采用 **Vibe Coding** 方式构建——以 Claude AI 作为全程配对编程伙伴，从产品设计、技术选型到逐行代码实现，全程 AI 协同。这种开发模式使得一个人能够完成通常需要整个团队才能交付的生产级全栈项目：自定义 CMS 主题、国际 SEO 体系、双语路由、CI/CD 自动部署，以及持续的功能迭代。

Vibe Coding 不是用 AI 生成代码后粘贴，而是将 AI 作为真正的技术伙伴——理解业务需求、权衡技术方案、发现潜在问题，并在整个项目生命周期中保持对代码库的深度上下文理解。

---

<div align="center">

*© 2025 · Built by Glory with Vibe Coding · All Rights Reserved*

</div>
