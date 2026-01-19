# zhurong2020.github.io 开发约定

GitHub Pages 静态博客站点，由 Gridea 生成的历史文章存档。

## 项目概述

- **定位**: 有心 (原有心言者) 博客的 GitHub Pages 静态站点
- **技术栈**: 纯静态 HTML (Gridea 生成)
- **在线地址**: https://zhurong2020.github.io
- **GitHub**: https://github.com/zhurong2020/zhurong2020.github.io
- **文章数量**: 86 篇

## Workspace 集成

### 与 Workshop 的关系
- **历史内容**: 包含 80 篇从 Gridea 迁移的原始文章
- **内容整合**: 三网合一策略中作为引流入口
- **主站迁移**: 主要内容已迁移到 WordPress (arong.eu.org)

### 当前定位
- 作为 SEO 引流页面
- 保留历史文章存档
- 通过 AdSense 进行变现尝试

## 项目特点

- **纯静态**: Gridea 客户端生成，无需本地构建
- **SEO 优化**: sitemap.xml, robots.txt, ads.txt 完整配置
- **AdSense 集成**: 已配置广告代码 (pub-3677908378517538)

## 目录结构

```
zhurong2020.github.io/
├── index.html        # 首页
├── 404.html          # 404 页面
├── sitemap.xml       # 站点地图 (SEO)
├── robots.txt        # 爬虫指引
├── ads.txt           # AdSense 配置
├── atom.xml          # RSS 订阅
├── post/             # 文章目录 (86 篇)
├── post-images/      # 文章图片
├── images/           # 站点图片
├── media/            # 媒体文件
├── styles/           # CSS 样式
├── tag/              # 标签页面
├── tags/             # 标签目录
├── archives/         # 归档页面
├── page/             # 分页 (5页)
└── TODO.md           # 任务清单
```

## 维护说明

### 内容更新
此站点为静态存档，不再通过 Gridea 更新。如需发布新文章：
1. 优先发布到 WordPress (arong.eu.org)
2. 可选：在此站点发布摘要并链接到主站

### 部署
- 推送到 main 分支自动触发 GitHub Pages 部署
- 无需构建步骤

### AdSense 状态
- 已提交审核
- 验证文件: ads.txt

## 注意事项

- 此站点为只读存档，不建议大规模修改
- 图片资源在 `post-images/` 目录
- atom.xml 文件较大 (325KB)，包含完整文章内容
