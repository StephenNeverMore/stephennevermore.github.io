# Shared developer website and app-ads.txt

多个应用共用的开发者网站与广告库存授权配置。

- Developer website: https://stephennevermore.github.io/
- Authorization file: https://stephennevermore.github.io/app-ads.txt

## 多个应用共用

各应用的 Google Play 开发者网站均可填写上述根域名。使用同一个 AdMob 发布商账号的应用共用现有的 Google 授权记录，无需按 App 重复添加。

如果以后使用其他发布商账号或广告网络，将对应平台提供的授权记录逐行追加到根目录的 `app-ads.txt`，不要覆盖现有记录。

## 发布约定

- 保留仓库名 `stephennevermore.github.io`，这是 GitHub Pages 用户根站点的命名要求。
- GitHub Pages 使用 `main` 分支的根目录发布。
- 保留 `.nojekyll`，`app-ads.txt` 必须作为 UTF-8 纯文本发布，不要加入 HTML、Markdown 代码块或 YAML 头。
- 不要重新启用旧 `app-ads.txt` 项目仓库的 Pages 发布，否则它会与根目录文件路径冲突。
- 应用介绍或隐私政策可分别维护在各自路径下；网站首页并不是隐私政策。

修改后检查公开文件返回 HTTP 200、`text/plain`，且内容与平台提供的记录一致，再到 AdMob 检查更新。
