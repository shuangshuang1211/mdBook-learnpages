此仓库包含使用 mdBook 框架创建的书籍项目，演示了如何自动部署书籍到 GitHub Pages。

## 项目概览

本项目利用 mdBook，一个用于从 Markdown 文件创建现代在线书籍的工具。我们的目标是自动化构建和部署流程，以便每次更新内容时都能快速发布到 GitHub Pages 上。

## 如何使用

要在本地构建和预览书籍，请确保已安装 [Rust](https://www.rust-lang.org/) 和 mdBook。然后，克隆此仓库并运行以下命令：

```
clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
mdbook serve
```

打开浏览器访问 `http://localhost:3000` 查看书籍。

## 自动部署流程

我们通过 GitHub Actions 实现了 CI/CD 流程，自动将书籍部署到 GitHub Pages。以下是部署流程的概述：

1. **推送更改**：将更改推送到 `main` 分支。
2. **GitHub Actions 触发**：基于 `.github/workflows/deploy.yml` 中定义的工作流程，GitHub Actions 会自动触发构建过程。
3. **构建书籍**：GitHub Actions 会安装 mdBook，然后构建书籍内容。
4. **部署到 GitHub Pages**：构建完成后，书籍会自动部署到 GitHub Pages。

你可以在 GitHub 仓库的 "Actions" 选项卡下查看工作流程的执行情况。

