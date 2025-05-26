# 🤝 协作者开发指南：SpiritWing 说明文档
欢迎参与维护和完善本项目文档！本文档将帮助你快速了解协作流程。

## 📦 项目简介
项目名称：杭州兵智-雷达无人机 SpiritWing 说明文档

仓库地址：`https://github.com/hongliyulvliyu/spiritwing_doc`

预览地址：`https://hongliyulvliyu.github.io/spiritwing_doc/`

<br>

## 🔧 环境要求
- Python ≥ 3.8

- 推荐使用 Anaconda（支持虚拟环境）

- 安装依赖：
```bash
# 1. 克隆项目
git clone https://github.com/hongliyulvliyu/spiritwing_doc.git
cd spiritwing_doc

# 2. 创建虚拟环境
conda create -n mkdocs-env python=3.9
conda activate mkdocs-env

# 3. 安装 MkDocs 及主题
pip install mkdocs mkdocs-material
```
<br>

## 📂 文档修改与结构说明
✅ 文档编写：
在`docs`目录下编辑`.md`文件撰写内容，所有图片、压缩包等资源放在 `docs/assets/ `下，文件路径引用使用相对路径，例如：
```markdown
![无人机](assets/spiritwing.jpg)
[下载软件](assets/software.zip)
```

✅ 文档结构：
```
spiritwing_doc/
├── docs/               # 所有 Markdown 文档放在这里
│   ├── index.md        # 首页
│   ├── drone.md        # 无人机本体
│   ├── ground_station.md # 地面站软件
│   └── assets/         # 图片和文件资源（如 .jpg、.zip）
├── mkdocs.yml          # 文档配置文件
├── site/               # 自动生成的网站文件（无需手动编辑）

```

<br>


## 🧪 本地预览
在项目目录下运行：

```bash
mkdocs serve
```
浏览器访问 http://127.0.0.1:8000 查看文档效果。

<br>

## 📤 提交修改流程
> 所有协作者请通过以下流程进行修改和推送

✅ 修改流程：
```bash
# 1. 切换主分支
git checkout master

# 2. 拉取最新代码
git pull origin master

# 3. 创建新分支（可选）
git checkout -b update-xxx
```
✅ 提交修改：
```bash
# 添加并提交修改
git add .
git commit -m "更新了 xxx 部分内容"

# 推送到远程分支
git push origin update-xxx
```
✅ 创建 Pull Request（PR）
在 GitHub 页面上提交 Pull Request，合并到主分支

<br>


## 🚀 发布流程
管理员帐号执行：
```
mkdocs build
mkdocs gh-deploy
```
将文档部署到 GitHub Pages，并自动更新线上地址。

