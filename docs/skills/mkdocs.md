# MkDocs Material 极简教程

本网站使用 MkDocs Material 构建。

本文将简单介绍如何使用 mkdocs 搭建网页，为想对本项目进行二次创作、或想要搭建个人网页的读者朋友们提供一些帮助。我们推荐您阅读 [Material for MkDocs 官方文档](https://squidfunk.github.io/mkdocs-material/getting-started/)，以获取更多资料。

## 环境配置

我们推荐您使用 Python 的包管理器 `pip` 来安装 Material for MkDocs。此外，您也可以使用 `docker` 进行安装，但本文将不会提供这方面的教程。

您还需要注册一个 [GitHub](https://github.com/) 账号，并下载 [Git](https://git-scm.com/downloads)。本文默认您已有相关知识储备，因此不再详细介绍上述步骤。如果您对此一头雾水(bushi)，我们建议您**善于使用搜索引擎**，或者向身边的同学寻求帮助。

> 画饼：日后，本网站也将提供 GitHub、Git 等基础技能的使用教程，敬请期待！

## 安装 mkdocs

打开您的终端（例如 Git Bash），使用 `pip` 进行安装（我们推荐您在一个虚拟的 Python 环境中进行该操作，但如果您不懂什么是虚拟环境，请忽略这行提示）：

```
pip install mkdocs-material
```

## clone 本项目

新建一个文件夹，在该路径下打开终端，并输入

```
git clone https://github.com/WeiYangXueXi/WeiYangXueXi.github.io.git
```

该指令会把我们的 GitHub 仓库克隆到您的本地，以便您进行构建和部署。

## 搭建网站

输入如下指令，切换到 master 分支：

```
git checkout master
```

该分支包含了构建网站所需要的主要文件（大多是 `.md` 格式的文件，以及记录文件架构的 `.yml` 文件）。您可以直接对任意的 Markdown 格式文件进行修改，或在**清楚地明白您在做什么**的情况下，修改 `mkdocs.yml` 文件，随心所欲地二次创作。

此后，可以输入以下指令，搭建出一个静态网页：

```
mkdocs build
```

您还可以输入如下指令，在本地预览网页效果：

```
mkdocs serve
```

## 部署网站

您可以使用 GitHub Pages 等方式部署您的网站，从而让其他人看到您的作品。关于如何部署网站，[Material for MkDocs 官方文档](https://squidfunk.github.io/mkdocs-material/publishing-your-site/) 已然提供了相当详尽的说明。如果您先前没有相关知识或经验，我们相信您会在这个过程中获得很大的收获！

省流：您需要新建一个特定的 GitHub 仓库、在 `mkdocs.yml` 文件中进行相应配置，最后输入如下指令，方可成功部署：

```
mkdocs gh-deploy
```

当然，作为补充，本文仍将强调一个或许您已注意到的细节：在我们的 GitHub 仓库中，有两个主要的分支—— master 与 gh-pages。前者包含了大量的 Markdown 等源文件；而后者则将这些 Markdown 文件转换成了 HTML 格式，最终形成了我们所看到的网站。

如果您按照官方文档完成了相关配置，那么您在 master 分支输入 `mkdocs gh-deploy` 后，gh-pages 分支将自动更新并 push 到远程仓库、并部署到您的 GitHub Pages 上。Hmmmmm, very interesting!

至此，如果一切顺利（但往往不是），您可以访问 https://xxx.github.io（xxx 为您的 GitHub 用户名），看到您成功部署的网站！快把这个网站链接分享给您的朋友，让他们来访问吧！

## 补充阅读

您可以进一步阅读以下材料，以加深您对本文提到的相关知识的了解：

1. [MDN](https://developer.mozilla.org/zh-CN/)：一份我们认为不错的 Web 入门教程
2. [Hexo](https://hexo.io/)：搭建个人博客的一种框架
3. [Markdown](https://www.markdowntutorial.com/)：不会吧不会吧，难道还有人不在用 Markdown 做笔记？
