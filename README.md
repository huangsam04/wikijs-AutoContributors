# wikijs-AutoContributors
自动展示贡献者到页面最底端。

![样例照片](/example.png)

## 使用方式
1. 将/wikijs-contributors.js 上传到一个可以访问到的地方
2. 打开wiki.js后台，`系统` - `API 访问`处生成一个API Key。
3. 生成时选择的用户组应当**只有** `read:pages`和`read:history` 两个权限，**别给多了**！！
4. **警告**：密钥是公开的，任何访问到网页的人都能拿到这个API Key，请不要给予过多的权限。
5. 打开wiki.js后台，选择 `主题` - `代码注入` - `Head 部插入 HTML`
6. 输入如下内容：
```
<script
  src="此处填入脚本的链接，例如上传到wiki.js本站素材根目录的话就是/wikijs-contributors.js"
  data-api-key="此处填入API Key"
  data-graphql-url="https://你的wiki.js网址/graphql">
</script>
```
7. 点击 应用

## 原理
使用Chatgpt和Claude合璧生成（。

用到了graphql。

## 已知问题
1. 访问 / 时候无法显示贡献者，/zh/home 就正常运行。
