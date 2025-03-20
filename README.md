# 图库

1. 在 `content` 目录下创建文件夹（比如 2026）

2. 创建 `index.md` 文件

```yaml
---
description: 描述
keywords: [关键词1 关键词2]
categories: 2022 # 目录，会在首页图上面显示
title: 2023 # 图集标题
weight: 1 
menus: "main"
resources:
  - src: 3088dbdc9249291a890e0d54c9ca4267.JPG # 图集封面
    params:
      cover: true
---
```

3. 将图片放到目录下

4. `hugo server -D` 查看效果

5. 部署 github

```bash
git add .
git commit -m "update"
git push origin master
```

4. 同步到服务器

```bash
rsync -avuz --progress --delete -e 'ssh -p 1202' dist/ root@104.168.120.15:/opt/1panel/apps/openresty/openresty/www/sites/gallery.solejay.cn/index
```