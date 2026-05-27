# KML 技术博客

这是一个可以直接发布到 GitHub Pages 的静态博客首页。

## 发布到 GitHub Pages

1. 在 GitHub 创建一个新仓库，例如 `kml-blog`。
2. 把本目录内容提交并推送到该仓库。
3. 进入仓库 `Settings` -> `Pages`。
4. Source 选择 `Deploy from a branch`，Branch 选择 `main`，目录选择 `/root`。
5. Custom domain 填写 `yutoudawang.com`。
6. 等待 GitHub Pages 部署完成，再回到域名 DNS 控制台添加解析。

## DNS 解析

如果使用裸域名 `yutoudawang.com`，在域名 DNS 控制台添加 4 条 A 记录：

```text
主机记录: @    记录类型: A    记录值: 185.199.108.153
主机记录: @    记录类型: A    记录值: 185.199.109.153
主机记录: @    记录类型: A    记录值: 185.199.110.153
主机记录: @    记录类型: A    记录值: 185.199.111.153
```

如果同时使用 `www.yutoudawang.com`，添加一条 CNAME：

```text
主机记录: www    记录类型: CNAME    记录值: yutoudawang.github.io
```

DNS 生效后，在 GitHub Pages 设置中开启 `Enforce HTTPS`。
