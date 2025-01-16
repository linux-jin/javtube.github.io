# Home (简体中文)

![Plugin Banner](images/banner.png)

[English](README.md) | 简体中文

-----

**文档**: [https://metatube-community.github.io](https://metatube-community.github.io)

**社区**: [https://github.com/metatube-community](https://github.com/metatube-community)

-----

## 主要原理

- 通过`metatube-server`后端从相应[数据来源](./wiki/metadata-providers.md)爬取数据并保存在数据库中。
- 安装好的 MetaTube 插件通过扫描到的本地文件名，向`metatube-server`请求查询，并下载相应的元数据与图片。

> 其中，图像裁剪、人脸识别、自动翻译等诸多复杂的功能也均在服务端完成。

## 如何使用

- 第一步：[部署后端](./wiki/server-deployment.md)
- 第二步：[安装插件](./wiki/plugin-installation.md)

完整的文档以及使用方法，请参阅 [Wiki](./wiki/README.md)。

### 插件更新

- 通过存储库 URL 添加的插件，Jellyfin会在后台自动更新。
- Emby 版本的 MetaTube 插件会通过计划任务自动更新。

> 需要重启 Jellyfin/Emby/Plex 服务，插件才会生效。

### 插件配置

- 进入 MetaTube 插件所在的配置页面。
- 输入之前配置好的后端地址 URL 以及需要的后端密钥 Token。
- 进入需要使用插件的媒体库：
    - 务必选择`电影`作为媒体库类型。
    - 勾选`MetaTube`作为元数据下载器与图片获取器。

> 其他例如自动翻译、人脸识别等配置，可以参考右侧页面的相关内容。

### 具体使用

- 在添加完视频后，点击`扫描媒体库`按钮。
- 使用`刷新元数据`以更新数据内容。
- 使用`识别`手动搜索影片或演员数据。

### 演员头像

MetaTube 集成了内置的演员提供源，可以通过演员名自动地搜索以及识别演员信息。与其他同类插件不同，用户不需要做任何配置，插件会在后台完成所有的演员信息搜索匹配工作。

目前插件使用 [`GFriends`](https://github.com/xinxin8816/gfriends) 和 [`XsList`](https://xslist.org/zh) 作为演员信息与图片的提供源。

### 特别建议

- 规范化的文件名可以提高影片识别的准确度，具体请看[命名规范](./wiki/naming-rules.md)页面。
- 十分建议**仅**☑️勾选`MetaTube`作为媒体库的刮削源以避免一些元数据刮削问题。

### 关于代理

请看[代理配置](./wiki/proxy-configuration.md)页面。

## 问题反馈

> 遇到问题前可以先查看 [FAQ](./faq.md) 中是否已存在类似的问题。

- 如果你遇到任何的 BUG，欢迎来 [Issues](https://github.com/metatube-community/jellyfin-plugin-metatube/issues) 区提交。
- 如果你有任何其他的问题，可以来 [Discussions](https://github.com/metatube-community/jellyfin-plugin-metatube/discussions) 或加入 [TG群](https://t.me/MetaTubePlugin) 讨论。

<!-- ## 效果预览

[预览仅供参考](./previews/)。 -->

## 参与开发

如果你擅长 `C#`，`Python` 或 `Go` 语言且希望一同开发维护本项目，可以加入TG群讨论。

## 授权许可

本插件项目在 [MIT](https://github.com/metatube-community/jellyfin-plugin-metatube/blob/main/LICENSE) 许可授权下发行。此外，如果使用本项目表明还额外接受以下条款：

- 本插件仅供学习以及技术交流使用
- 请勿在公共社交平台上宣传此项目
- 使用本软件时请遵守当地法律法规
- 法律及使用后果由使用者自己承担
- 禁止将本软件用于任何的商业用途
