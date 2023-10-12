---
title: hexo 部署到github pages关键步骤
date: 2023-10-12 11:03:06
tags:
---
1.hexo工程文件，博客内容的markdown文件，需要保存在一个分支。而生成的静态网站，需要存放在另外分支。
2.生成的静态网站并且发布到另外一个分支，可以通过hexo的插件完成。

步骤1：
修改_config.yml文件，在最后加入以下配置：
  deploy:
    type: git
    repository: https://github.com/username/username.github.io
    branch: main


需要注意的发布分支bran需要和归档分支不同，发布分支需要和git仓pages设置中的分支一致

步骤2：
安装
npm install hexo-deployer-git --save

步骤3:
生成和发布
hexo clean 
hexo g 
hexo d