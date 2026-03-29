<img align="right" width="150" alt="logo" src="https://user-images.githubusercontent.com/5889006/190859553-5b229b4f-c476-4cbd-928f-890f5265ca4c.png">

# Hugo Theme Stack 入门模板

这是一个 [Hugo theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) 的快速入门模板。它使用 [Hugo modules](https://gohugo.io/hugo-modules/) 功能加载主题。

它包含一个基本的主题结构和配置。GitHub Action 已设置，可自动将主题部署到公共 GitHub 页面。此外，还有一个 cron 任务，可每天自动更新主题。

## 视频教程

如果您在设置过程中遇到任何问题，这里有一个视频教程，演示如何使用此模板设置一个新的 Hugo 站点并将其部署到 GitHub Pages：https://www.youtube.com/watch?v=8qDdQQ6Ifxo

## 开始使用

1. 点击“使用此模板”，在 GitHub 上创建名为 `<username>.github.io` 的仓库。（您也可以使用不同的仓库名称，但这样生成的网站将通过 `https://<username>.github.io/<repository-name>` 访问。）

![步骤 1](https://user-images.githubusercontent.com/5889006/156916624-20b2a784-f3a9-4718-aa5f-ce2a436b241f.png)

2. 创建仓库后，创建一个与其关联的 GitHub 代码空间。

![创建代码空间](https://user-images.githubusercontent.com/5889006/156916672-43b7b6e9-4ffb-4704-b4ba-d5ca40ffcae7.png)

3. 在等待代码空间创建完成期间，前往新创建的仓库的“设置”->“页面”，并将“构建和部署”->“来源”设置为“GitHub Actions”。

![更改构建和部署来源](https://github.com/user-attachments/assets/192459bf-25d8-441e-8029-c108d789e449)

4. 代码空间创建完成后，您可以在终端运行 `hugo server` 命令来测试网站是否构建成功，并查看新网站的运行情况。

5. 检查 `config` 文件夹以获取配置文件。您可以根据需要进行编辑。请务必将 `config/_default/config.toml` 文件中的 `baseurl` 属性更新为您网站的 URL。例如，如果您的新仓库名为 `my-blog`，则 `baseurl` 应为 `https://<username>.github.io/my-blog/`。

6. 完成网站编辑后，只需提交并推送即可。GitHub Action 会自动将网站部署到与该仓库关联的 GitHub Pages。

---

如果您不想使用 GitHub Codespace，也可以在本地计算机上运行此模板。 **您需要在本地安装 Git、Go 和 Hugo Extended。** 更多信息，请查看 Hugo 官方文档：https://gohugo.io/installation/

## 手动更新主题

运行：

```bash

hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v4

hugo mod tidy

```

> 此入门模板已配置为主题的 `v4` 版本。由于 Go 模块的限制，一旦主题发布了 `v4` 或更高版本，您需要手动更新主题（修改 `config/module.toml` 文件）。

## 部署到其他静态页面托管平台

请查看 Hugo 官方文档：https://gohugo.io/host-and-deploy/