# 夏麒义个人作品集网站

学号：2026116040198　姓名：夏麒义

## 项目简介
本项目是一个静态个人作品集网站，用于展示个人介绍、课程项目、实践经历、图片作品和博客文章。网站采用多页面结构，包含首页、作品/文章列表页、详情页和关于页，并通过少量原生 JavaScript 实现图片轮播、分类筛选、关键词搜索和反馈表单提示。

## 技术栈
- HTML5 / CSS3 / 原生 JavaScript
- Git + GitHub
- Linux + Nginx

## 目录结构
\`\`\`text
portfolio-site/
├── index.html
├── works.html
├── detail.html
├── about.html
├── css/style.css
├── js/main.js
├── assets/images/
└── README.md
\`\`\`

## 本地运行
直接双击 index.html 即可打开首页；也可执行 python -m http.server 8080 后访问 http://localhost:8080。

## 部署说明
\`\`\`bash
ssh [SSH用户]@[公网IP]
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
nginx -v
systemctl status nginx
sudo mkdir -p /var/www/portfolio
sudo chown -R $USER:$USER /var/www/portfolio
git clone [GitHub仓库地址] /var/www/portfolio
sudo nano /etc/nginx/sites-available/default
nginx -t
sudo systemctl reload nginx
cd /var/www/portfolio && git pull
\`\`\`
Nginx root 指向 /var/www/portfolio。注意：仓库设为公开，提交记录不少于 5 次，源码包不包含 .git 与 node_modules。
