
---

# 🌟 Git + VS Code 初学者教程（适用于 macOS）

适合对象：**零基础或初学者**，使用 Mac，想通过 VS Code 和 Git 来管理代码项目，并同步到 GitHub。

---

## 🧩 目录

1. [安装 Git 和 VS Code](#1-安装-git-和-vs-code)
2. [配置 Git](#2-配置-git)
3. [创建本地 Git 仓库](#3-创建本地-git-仓库)
4. [使用 VS Code 编写与管理代码](#4-使用-vs-code-编写与管理代码)
5. [连接到 GitHub 并推送代码](#5-连接到-github-并推送代码)
6. [日常 Git 操作命令](#6-日常-git-操作命令)
7. [常见问题 & 提示](#7-常见问题--提示)

---

## 1. 安装 Git 和 VS Code

### 🛠 安装 Git

1. 打开终端，输入：

   ```bash
   git --version
   ```

   如果提示未安装，继续执行下一步。

2. 使用 Homebrew 安装：

   ```bash
   brew install git
   ```

3. 安装完成后再次检查：

   ```bash
   git --version
   ```

### 📝 安装 VS Code

1. 访问官网：[https://code.visualstudio.com/](https://code.visualstudio.com/)
2. 下载 macOS 版本并安装
3. 打开后可以设置中文界面（Command + Shift + P → 输入 `Configure Display Language`）

---

## 2. 配置 Git

打开终端，执行以下命令设置你的身份：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱（用于 GitHub）"
```

可选设置（显示美化）：

```bash
git config --global color.ui auto
```

查看配置：

```bash
git config --list
```

---

## 3. 创建本地 Git 仓库

### ✅ 新建项目

1. 在 Finder 中创建文件夹，例如 `Awesome Mac for CS`
2. 用 VS Code 打开此文件夹

   ```bash
   code "Awesome Mac for CS"
   ```

### 🚀 初始化 Git 仓库

在 VS Code 中打开终端，输入：

```bash
git init
```

### ✍️ 创建文件

新建文件，例如：

* `README.md`
* `Git Tutorial for Beginners.md`
* `homebrew.ipynb`

保存这些文件后，使用以下命令：

```bash
git add .
git commit -m "Initial commit with tutorial and notes"
```

---

## 4. 使用 VS Code 编写与管理代码

* 左侧源代码管理图标可以查看未提交更改
* 可以用 Markdown 编辑器编写教程
* `.ipynb` 文件可以用 Python 插件打开（推荐安装 Jupyter 插件）

---

## 5. 连接到 GitHub 并推送代码

### 📦 创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 创建新仓库（仓库名建议与文件夹一致）

### 🔗 连接远程仓库

在 VS Code 终端中执行：

```bash
git remote add origin https://github.com/你的用户名/你的仓库名.git
git branch -M main
git push -u origin main
```

如果提示验证身份，可以登录 GitHub 并设置 [Personal Access Token](https://github.com/settings/tokens)

---

## 6. 日常 Git 操作命令

| 功能     | 命令                          |
| ------ | --------------------------- |
| 查看状态   | `git status`                |
| 添加文件   | `git add 文件名` 或 `git add .` |
| 提交更改   | `git commit -m "说明"`        |
| 查看日志   | `git log`                   |
| 推送到远程  | `git push`                  |
| 拉取远程更新 | `git pull`                  |
| 查看分支   | `git branch`                |
| 创建新分支  | `git checkout -b 分支名`       |
| 切换分支   | `git checkout 分支名`          |

---

## 7. 常见问题 & 提示

### ❓ VS Code 终端是 zsh，和 bash 有区别吗？

默认 macOS 使用 zsh，和 bash 在 Git 操作上没有区别。

### ❓ `.venv` 是什么？

是 Python 的虚拟环境目录。记得在 `.gitignore` 中加上一行：

```
.venv/
```

### 🔧 推荐安装 VS Code 插件

* GitLens — 提供强大的 Git 历史追踪功能
* Markdown All in One — 编写教程更方便
* Python & Jupyter — 支持 `.ipynb` 文件

---

如果你希望我将此教程导出为 Markdown 文件，或者想将其附加到你的项目里（比如 `Git Tutorial for Beginners.md`），我可以为你生成内容文件。是否需要？
