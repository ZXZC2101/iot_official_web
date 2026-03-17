# iot_official_web

实验室官网静态站点，当前以 `PHP + HTML + CSS + jQuery` 组织，无额外构建流程。

## 目录结构

- `index.php`：首页
- `project_show.php`：项目展示页
- `css/`：样式文件
- `img/`：图片与 Logo 资源
- `font/`：站点字体
- `js/jQuery/`：本地 jQuery 依赖

## 本地运行

在仓库根目录执行：

```bash
php -S localhost:8000
```

然后访问：

```text
http://localhost:8000/index.php
```

## 维护说明

- 这是一个无构建步骤的静态/轻量 PHP 站点。
- 修改页面后，至少检查 `index.php` 和 `project_show.php` 是否能正常加载。
- 提交前可执行语法检查：

```bash
php -l index.php
php -l project_show.php
```
