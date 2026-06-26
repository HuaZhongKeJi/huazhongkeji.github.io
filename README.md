# GitHub Pages 发布说明

这个目录可以直接作为 GitHub Pages 静态站点使用，用于提供 Edge 插件上架需要的公开 URL。当前页面内容已按扩展 1.0.4 更新。

## 发布方式一：网页上传

1. 登录 GitHub。
2. 新建一个 Public 仓库，例如 `medical-conversation-capture-pages`。
3. 上传本目录中的 `index.html`、`privacy.html`、`support.html`、`README.md`。
4. 进入仓库 `Settings`。
5. 打开 `Pages`。
6. `Build and deployment` 选择 `Deploy from a branch`。
7. `Branch` 选择 `main`，目录选择 `/root`。
8. 保存后等待 GitHub 生成页面。

生成后的 URL 通常是：

```text
https://你的GitHub用户名.github.io/仓库名/
https://你的GitHub用户名.github.io/仓库名/privacy.html
https://你的GitHub用户名.github.io/仓库名/support.html
```

在 Microsoft Partner Center 中填写：

```text
Privacy policy URL: https://你的GitHub用户名.github.io/仓库名/privacy.html
Support URL: https://你的GitHub用户名.github.io/仓库名/support.html
Website: https://你的GitHub用户名.github.io/仓库名/
```

## 发布方式二：Git 命令

在本目录执行：

```powershell
git init
git branch -M main
git add .
git commit -m "Add extension public pages"
git remote add origin https://github.com/你的GitHub用户名/medical-conversation-capture-pages.git
git push -u origin main
```

然后按“发布方式一”的第 4 步到第 8 步开启 GitHub Pages。

## 提交语言

Edge Add-ons 商店资料可以使用中文。面向中国参与者、中文问卷和中文扩展说明时，中文材料是合理的。

建议同时准备一段英文审核备注，便于非中文审核人员理解扩展用途。英文不是所有字段的强制要求，但中英双语通常能降低审核沟通成本。

## 提交前需要替换的内容

- 支持邮箱已填写为 `sun@njmu.edu.cn`。
- 发布主体名称已填写为“南京医科大学医政学院数智健康治理研究课题组”，提交前请确认该名称可公开展示。
- 课题负责人：孙振宇。
- 办公地址已填写为“江苏省南京市江宁区龙眠大道101号 南京医科大学医政学院，邮编211166”。
- 数据保留期限。
- 参与者撤回、删除或更正请求流程。
- 伦理审查信息：南京医科大学伦理委员会，南医大伦审〔2026〕92号，2026年5月27日。
- 当前上传接口已调整为 `https://okrtest.hq-opt.com/api/chat/plugin/latest`；问卷上下文读取域名仍为 `http://122.152.221.80/*`。


