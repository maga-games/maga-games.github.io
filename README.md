# maga-games.github.io

**maga-games.com** 的精简预览站（方案 C）：单页 landing，精选游戏外链至主站试玩。

**Live site:** https://maga-games.github.io

## 定位

- 展示 6 款精选装扮/美妆/美甲类游戏
- 点击游戏 → 跳转 `https://maga-games.com/play/:slug` 试玩
- 不做本地 iframe 玩法页，避免与主站 SEO 竞争

## 文件结构

```
index.html      # 唯一页面
css/style.css   # 样式（沿用主站品牌色）
favicon.svg     # 站点图标
robots.txt
sitemap.xml     # 仅含首页
.nojekyll       # GitHub Pages 静态部署
```

**Analytics:** GA4 `G-3VCEG1CQBJ`（gtag，见 `index.html` `<head>`）

## 本地预览

```bash
# Python
python3 -m http.server 8080

# 或 npx
npx serve .
```

打开 http://localhost:8080

## 部署

推送到 `main` 分支后，在 GitHub 仓库 **Settings → Pages** 中选择 **Deploy from branch → main / root**。

## 更新精选游戏

编辑 `index.html` 中 `.game-grid` 区块：替换游戏名、图标 URL、标签和 `maga-games.com/play/:slug` 链接。游戏数据可参考主站 `games.json` 与 `src/config/site.ts` 的 `homepage.bannerSlugs`。
