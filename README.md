# 持久微信群二维码

本仓库托管微信群入群二维码。固定入口会读取最新版 `group.png`、在浏览器内解析其中的微信链接并自动跳转，因此群二维码每周更新时无需更换固定入口码。

## 固定入口

入口页面：<https://sii-zhangyifei.github.io/group-qr/>

![持久入群二维码](./persistent-group-qr.png)

在其他项目的 README 中可使用：

```markdown
[![扫码进群](https://raw.githubusercontent.com/SII-ZhangYiFei/group-qr/main/persistent-group-qr.png)](https://sii-zhangyifei.github.io/group-qr/)
```

## 更新方式

`group.png` 由自动化流程每周更新。入口页会优先读取 `main` 分支的最新图片；`persistent-group-qr.png`、Pages 分支和 `index.html` 都不需要跟着修改。GitHub 图片缓存偶尔需要几十秒到几分钟刷新。

中转页内置 ZXing 解析器，不向第三方解码服务上传图片，并且只允许跳转到 `https://weixin.qq.com/g/`。
