# 星露谷数据手册

纯前端静态攻略，包含作物种植、加工收益、鱼类及动物养殖资料。

- 在线攻略：https://girlskk.github.io/stardew-guide/
- 个人账号仓库：https://github.com/girlskk/stardew-guide

## 本地使用

直接用浏览器打开 `index.html`。数据、样式和脚本已内嵌，无需安装依赖或运行构建命令。

## GitHub Pages

将本仓库上传到 GitHub 后，在仓库 **Settings → Pages** 中选择：

- Source：Deploy from a branch
- Branch：main
- Folder：/ (root)

保存后，等待 GitHub 完成部署，并使用 Pages 设置页给出的网站地址。

`.nojekyll` 用于将网站作为普通静态文件发布。

## 更新攻略

如果修改的是本地原始文件 `星露谷数据手册.html`，先将它复制为 `index.html`，再提交并推送到 `main`。原始副本保留在本地，不重复上传。

在 PowerShell 中执行：

```powershell
Set-Location 'C:\Users\rli18\Documents\Stardew Valley'
# 如果已直接修改 index.html，则跳过下面的复制命令。
Copy-Item -LiteralPath '星露谷数据手册.html' -Destination 'index.html'
git add -- index.html
git commit -m '更新攻略数据'
git push
```

推送后，GitHub Pages 会自动更新网站，网址保持不变。可以在仓库的 Actions 页面查看发布结果。

网站内容为原版与特定模组、存档配置下的数据快照；具体适用条件以页面内说明为准。
