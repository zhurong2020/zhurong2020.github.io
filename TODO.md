# Gridea-Blog 项目待办清单

**最后更新**: 2026-04-15
**项目状态**: 维护模式（新内容已迁移至 WordPress）
**负责人**: zhurong

---

## 优先级说明
- P0: 紧急/安全相关
- P1: 本周完成
- P2: 本月完成
- P3: 可选/低优先级

---

## 待办事项

### P0 - AdSense 账号停用预警（2026-10-03 收到 · 约 11-02 前处理）

Google 邮件：发布商 `pub-3677908378517538` 未激活，30 天后停用（停用后可重新启用）。
**2026-10-03 后台诊断**（诸嵘用浏览器端 Claude 插件查看，本地 Claude Code 复核了能从外部看到的部分）：

| 项目 | zhurong2020.github.io | arong.eu.org |
|---|---|---|
| 网站所有权验证 | ✅ | ✅ |
| 页面广告代码 `ca-pub-3677908378517538` | ✅ | ✅ |
| 线上 `ads.txt` | ✅ 200 | ✅ 200（本地复核：`https://arong.eu.org/ads.txt` 直接 200、**不跳转**，`www` 也 200 → 插件建议的「改 Nginx 让裸域直出」不需要做） |
| 后台审批 | ❌ 需要注意：低价值内容 | ❌ 需要注意：低价值内容 |
| 后台 ads.txt 显示 | 「未找到」（记录停在 2026-05，旧抓取） | 「未找到」（记录停在 2026-04） |

账号顶部提示「需要添加收款信息并激活账号」。

- [ ] **诸嵘先定：保留还是放弃 AdSense**。放弃 → 不用处理，任其停用，之后从两站撤广告代码与 `ads.txt`。保留 → 按下面做。
- [ ] **激活账号**（诸嵘本人）：后台点「激活账号」，填收款/银行信息。这一步能阻止 30 天停用，与网站审核相互独立。
- [ ] **github.io 内容整改**：最新文章 2025-09，一年多未更新，大概率是「低价值」主因。发几篇 1500 字以上的原创实践文；合并或删除短文、重复和转载文（2026-04 已给 9 篇加 noindex）；每篇写清标题、摘要和内部链接；`sitemap.xml` 只留有实质内容的页面，再到 Search Console 重新提交。
- [ ] **arong.eu.org 内容整改**（WordPress + Elementor，411 篇）：标签、分类、分页页面用 Yoast 设 noindex；短文和重复文合并或设 noindex；排查 AI 批量生成或自动转载的文章；确认「关于我」「隐私政策」可访问，补一个「联系方式」页；审核通过前不放手动广告位。
- [ ] **申请重新审核**（内容整改完成后再提交，否则容易再次被拒）：AdSense → 网站 → 勾「我确认已解决相关问题」→ 申请审核，两站分别提交。审核要几天到几周。
- [ ] 通过后：广告 → 按网站，分别开启自动广告；收入在「报告 → 按网站」里看。

### P0 - 紧急任务（AdSense 违规修复）- 已完成 2026-01-11

**问题描述**: Google AdSense 显示"您的网站尚未准备好展示广告"，需要修复合规问题。

**诊断结果**: 缺少必要的法律页面

- [x] **创建隐私政策页面** (2026-01-11)
  - 路径: `/post/privacy-policy/index.html`
  - 包含: GA/AdSense 数据收集说明、Cookie 政策、用户权利

- [x] **创建服务条款/免责声明页面** (2026-01-11)
  - 路径: `/post/terms-of-service/index.html`
  - 包含: 投资风险免责声明、非专业建议声明、责任限制

- [x] **创建联系方式页面** (2026-01-11)
  - 路径: `/post/contact/index.html`
  - 包含: 联系邮箱 zhurong2020@gmail.com、社交媒体链接

- [x] **更新导航菜单** (2026-01-11)
  - 首页和关于页面已添加: 隐私政策、服务条款、联系我们 链接

### P1 - 本周任务 - 已完成 2026-01-11

- [x] **创建 robots.txt** (2026-01-11)
  - 路径: `/robots.txt`

- [x] **创建 sitemap.xml** (2026-01-11)
  - 包含 84 个页面（首页、归档、标签 + 81 篇文章 + 3 个新页面）

### P1 - 本周任务（2026-04 批次）

- [x] **AdSense 低价值内容第二轮整改** (commit 6259c08, 2026-04-14)
  - 触发: AdSense 后台 2026-02-10 标记 "需要注意 · 低价值内容"
  - 9 篇薄内容旧文注入 `<meta name="robots" content="noindex,follow">`:
    - `du-cai-yu-...ba-fei-te-fen-shou` (1337 字)
    - `ps-xue-xi-ji-lu` (1397 字)
    - `tui-jian-yi-ge-ying-yu-...-aboboo` (1441 字)
    - `jin-nian-yao-ren-zhen-wan-cheng-de-du-shu-ren-wu-qing-jian-du` (1677 字)
    - `jin-ri-qi-dong-youtube-de-a-rong-excel-pin-dao-...` (1801 字)
    - `wei-yi-ji-hua-kai-shi-ben-wen-zhi-gei-zi-ji-kan-...` (2131 字，"本文只给自己看")
    - `chong-qi-boox-de-guan-jian-gong-neng-chuan-shu` (2136 字)
    - `ps-xue-xi-ji-lu-shang-ye-she-ji-shi-zhan-zhu-tu-pian-02` (2163 字)
    - `you-wto-guan-yu-xin-guan-yi-miao-...-de-xin-wen-xiang-dao-de` (2185 字)
  - sitemap.xml 同步剔除：87 → 78 URL
  - 隐私政策扩写：2396 → 4421 字符（新增 DART Cookie / NAI / DAA / GDPR / CCPA / GA4 退出）
  - 服务条款扩写：补全投资风险/技术工具免责、责任限制、适用法律
  - 成效：AdSense 状态由 "需要注意" 变为 "正在准备"

- [ ] **AdSense ads.txt 抓取状态复核（72h 后）**
  - 当前: ads.txt 列显示 "未找到"（Google AdsBot 滞后抓取，非实际问题）
  - 实际: `https://zhurong2020.github.io/ads.txt` HTTP 200 + text/plain + `ca-pub-3677908378517538` ✓
  - 复核日期: 2026-04-17
  - 同步 arong.eu.org 一起复核，详见 /home/zhurong/vps-server/TODO.md P1

### P2 - 本月任务

- [ ] **添加 Open Graph Meta Tags**
  - 改善社交媒体分享预览效果

### P3 - 可选任务

- [ ] **强化投资文章免责声明**
  - 在所有 16 篇投资相关文章顶部添加显著免责声明

- [ ] **重审通过后的后续动作**
  - 决定是否删除（而非仅 noindex）9 篇薄文
  - 评估其余 <2500 字旧文（about / contact / privacy / terms 除外）是否也要 noindex 或补充内容
  - 考虑把 9 篇薄文的 noindex 在重审通过后保留一段时间再决定

---

## 当前网站状态（2026-04-15 更新）

| 检查项 | 状态 | 说明 |
|--------|------|------|
| 文章数量 | 84 篇（9 篇 noindex） | 可索引 75 篇 |
| About 页面 | 存在 | `/post/about` |
| 隐私政策 | ✅ 完善版 (4421 字符) | DART/NAI/DAA/GDPR/CCPA 齐全 |
| 服务条款 | ✅ 完善版 (3867 字符) | 投资/技术免责 + 责任限制 |
| 联系页面 | 存在 | `/post/contact` |
| AdSense 代码 | 已安装 | ca-pub-3677908378517538 |
| ads.txt | 存在 | 正确配置（AdSense 后台显示 "未找到" 为抓取滞后） |
| robots.txt | 存在 | 允许全部爬取 |
| sitemap.xml | 78 URL | 剔除 9 个 noindex 薄文后的数量 |
| AdSense 审核 | 正在准备 | 2026-04-14 重新提交 |

---

## 已完成任务

### 2026-04-14
- [x] 第二轮 AdSense 低价值内容整改（9 篇薄文 noindex + 隐私/条款扩写，commit 6259c08）

### 2026-01-08
- [x] 部署 AdSense ads.txt
- [x] 部署 AdSense 验证代码

---

## 备注

由于新内容创作已迁移至 WordPress (www.arong.eu.org)，本项目主要任务是：
1. 修复 AdSense 合规问题
2. 保持现有内容可访问
3. 不再发布新文章
