# Roina Tours — 静态网站

## 文件结构
```
roinatours-site/
├── index.html          首页
├── about.html          关于我们
├── products.html        产品/目的地详情(西安/上海/北京/重庆)
├── smart-model.html     SMART 模型
├── contact.html         联系我们
├── css/style.css        全站样式
└── js/main.js           移动端菜单交互
```

## 部署到 GitHub Pages
1. 在 GitHub 新建一个仓库,比如 `roinatours-site`
2. 把这个文件夹里的所有文件上传到仓库根目录(直接拖拽上传或用 git push 都可以)
3. 进入仓库 Settings → Pages
4. Source 选择 `Deploy from a branch`,Branch 选择 `main` / `/(root)`
5. 保存后等 1-2 分钟,页面会显示一个 `https://你的用户名.github.io/roinatours-site/` 的网址
6. 如果想绑定自己的域名(比如 roinatours.com),在同一个 Pages 设置页面填入 Custom domain,再去域名服务商那边加一条 CNAME 记录指向 `你的用户名.github.io`

## 替换占位图片
所有标记 `[ ... photo ]` 的灰绿色块都是占位符,在 `css/style.css` 里对应 `.placeholder` 样式。
替换方法:
1. 把真实图片放进一个新建的 `img/` 文件夹
2. 找到对应的 `<div class="... placeholder">[ ... ]</div>`,改成:
   ```html
   <img src="img/xian.jpg" alt="西安城墙">
   ```
   (不需要再加 placeholder 相关 class)

## 之后要加登录/表单
- 简单联系表单 → 用 Formspree(免费),不需要自己搭后端
- 登录/账号系统 → Supabase Auth 或 Firebase Auth,前端引入它们的 JS SDK 即可
