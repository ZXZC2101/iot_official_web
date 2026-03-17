# iot_official_web

实验室官网静态站点，当前页面由 `HTML + CSS + jQuery` 组成，无构建流程。

## 页面入口

- `index.html`：GitHub Pages 静态部署首页
- `project_show.html`：GitHub Pages 静态部署项目展示页
- `index.php`：本地 PHP 调试用首页副本
- `project_show.php`：本地 PHP 调试用项目展示页副本

## 目录结构

- `css/`：样式文件
- `img/`：图片与 Logo 资源
- `font/`：站点字体
- `js/jQuery/`：本地 jQuery 依赖
- `source/`：页面引用的下载资源

## GitHub Pages 部署

GitHub Pages 不支持执行 PHP，因此仓库已提供静态入口：

- 首页使用 `index.html`
- 页面跳转使用 `.html` 链接

发布时将仓库根目录设置为 Pages 来源即可。

## 本地运行

如果需要按原来的方式本地预览，可以在仓库根目录执行：

```bash
php -S localhost:8000
```

然后访问：

```text
http://localhost:8000/index.php
```

如果只是查看静态页面，也可以直接打开 `index.html`。

## 维护说明

- GitHub Pages 相关修改请优先同步到 `index.html` 和 `project_show.html`
- 如果仍需保留本地 PHP 预览，修改后请同步检查对应 `.php` 文件
- 提交前至少确认首页和项目展示页资源路径正常
