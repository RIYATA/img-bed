# img-bed · GitHub 图床

公开图床仓库，配合 [jsDelivr CDN](https://www.jsdelivr.com/) 生成图片直链，可在博客、Markdown 笔记、Typora 等任何地方直接引用。

## 目录结构

```
img-bed/
└── img/        ← 图片统一放这里
```

## 直链格式

图片推送到仓库后，直链规则：

```
https://cdn.jsdelivr.net/gh/RIYATA/img-bed@main/img/文件名.扩展名
```

示例（假设上传了 `img/2026/test.png`）：

```
https://cdn.jsdelivr.net/gh/RIYATA/img-bed@main/img/2026/test.png
```

> `@main` 表示 main 分支的最新内容，推送后即生效（首次访问可能有 1~2 分钟 CDN 缓存延迟）。

## 大陆访问备用域名

`cdn.jsdelivr.net` 在大陆可能不稳定，以下镜像域名路径完全相同，替换域名即可：

| 域名 | 示例 |
|---|---|
| `fastly.jsdelivr.net` | `https://fastly.jsdelivr.net/gh/RIYATA/img-bed@main/img/test.png` |
| `testingcf.jsdelivr.net` | `https://testingcf.jsdelivr.net/gh/RIYATA/img-bed@main/img/test.png` |
| `gcore.jsdelivr.net` | `https://gcore.jsdelivr.net/gh/RIYATA/img-bed@main/img/test.png` |

## 上传方式

1. **命令行**：图片放入 `img/` 后 `git add . && git commit -m "add images" && git push`
2. **PicGo**：图床选 GitHub，仓库名填 `RIYATA/img-bed`，分支 `main`，自定义域名填 `https://cdn.jsdelivr.net/gh/RIYATA/img-bed@main`，上传后自动生成 jsDelivr 直链
3. **网页**：GitHub 仓库页 → `img/` 目录 → Add file → Upload files

## 注意事项

- jsDelivr 对 GitHub 单文件限制 **20MB**，建议图片压缩后再上传（推荐 [Squoosh](https://squoosh.app/)）
- 仓库是公开的，**不要上传含个人隐私/敏感信息的图片**
- 图片已上传后如需替换内容，建议换文件名重新上传（jsDelivr 有缓存，同名覆盖可能长时间不更新）

> AI生成
