  ### 想拥有一个自己的博客，但不想花钱买服务器、不想折腾备案？GitHub Pages 完美解决这些问题——完全免费、
  自带 HTTPS、写完文章自动部署，甚至不需要你会写代码。
  本文用 5 分钟带你从零搭一个能用的博客，手把手操作。

  ### 一、为什么选 GitHub Pages
• 零成本：GitHub 免费提供站点托管和自动构建，没有流量限制。
• 自带域名和 HTTPS：地址就是 你的用户名.github.io，SSL 证书自动签发。
• Markdown 写文章：不需要后台系统，写完直接提交，自动生成网页。
• 数据归你所有：所有文章以文件形式保存在你的 GitHub 仓库里，永远不会丢，也不受任何平台限制。

### 二、3 步搭好博客
第 1 步：创建仓库
登录 GitHub，点击右上角 + → New repository，仓库名填 你的用户名.github.io（比如 zhangsan.github.io），选 Public，勾上 "Add a README file"，点击创建。
第 2 步：启用 Pages
进入仓库 → Settings → Pages，在 "Build and deployment" 里 Source 选 Deploy from a branch，Branch 选 main，文件夹选 / (root)，保存。一分钟后访问 https://你的用户名.github.io 就能看到页面了。
第 3 步：安装博客系统
手写 HTML 太麻烦，推荐用现成的静态博客框架。
以 Gmeek 为例（它直接用 GitHub Issues 当文章编辑器，手机也能写）：
1. 打开 [Gmeek 模板仓库](https://github.com/Meekdai/Gmeek-template)，点击 Use this template → Create a new repository
2. 仓库名随便填，勾选 Public
3. 进仓库 Settings → Pages，Source 选 GitHub Actions
4. 去 config.json 里改一下博客标题和头像
5. 在仓库 Issues 里新建一条 Issue，写点内容，标签选 blog
6. 等 1-2 分钟，GitHub Actions 自动构建完成，博客就上线了

### 三、可选：绑定自己的域名
如果你有独立域名，在仓库 Settings → Pages → Custom domain 填入域名，再去域名后台添加一条 CNAME 记录指向 你的用户名.github.io，勾选 Enforce HTTPS 即可。全程不需要备案。

### 四、写什么？
博客搭好了，最常遇到的问题反而是"不知道写什么"。几个方向供参考：• 学技术过程中的踩坑笔记• 工作中解决问题的思路记录• 常用工具、软件的推荐和对比• 读书笔记、学习心得别追求每篇都"完美"，先写起来。你的博客是你自己的地盘，怎么写由你说了算。