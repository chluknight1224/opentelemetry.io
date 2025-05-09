---
title: 公告
description: 为特别活动制作公告或横幅。
aliases: [/announcements, /docs/announcements]
weight: 50
---

公告是包含在某个区域的 “公告” 部分下的一个_常规的 Hugo 页面_。这意味着我们利用 Hugo 对页面日期（未来或已过期）、国际化等方面的内置处理功能，
来根据构建日期自动显示或隐藏横幅，确定横幅的排序，并处理回退到英文横幅等情况。
> 公告目前仅被用作横幅。我们最终_有可能……_
> 也会稍微多支持更通用一些的公告。

### 创建一则公告 {#creating-an-announcement}

要添加一条新的公告，请使用以下命令在本地化项目的 `announcements` 文件夹下创建一个公告的 Markdown 文件。:

```sh
hugo new --kind announcement content/YOUR-LOCALE/announcements/announcement-file-name.md
```

根据你期望的区域设置和文件名进行调整。将公告文本添加为页面的主体内容。

> 对于横幅而言，公告的主体内容应该是一个简短的短语。

{{% alert title="对于本地化来说" %}}

如果你正在创建一个**特定区域的公告覆盖内容**，请确保你使用与英文公告**相同的文件名**。

{{% /alert %}}

### 公告列表 {#announcement-list}

当构建日期处于公告的 `date` 字段和 `expiryDate` 字段之间时，任何给定的公告都会在网站构建中显示。
如果这些字段缺失，那么 “日期” 字段将被假定为 “当前时刻”，“到期日期” 字段将被假定为 “永远（无到期时间）”。

公告将按照由 Hugo 的 [Regular pages] 函数所确定的标准页面顺序显示。也就是说，（按 `weight` 来算）“权重最小”的公告将最先显示。
当权重相同或者未指定权重时，（按 `date` 来算）最新的公告将最先显示，诸如此类。

所以，如果你想让一则公告显示在最上方，就在前置内容中使用一个负的 `weight` 值。

如果你发现这个仓库的内容存在错误或问题，或者你希望请求进行功能增强，请 [创建一个 issue][new-issue]。

如果你发现了一个安全问题，在提交问题之前，请阅读[安全策略](https://github.com/open-telemetry/opentelemetry.io/security/policy)。

在报告新问题之前，请务必通过查阅我们的 [issue 列表](https://github.com/open-telemetry/opentelemetry.io/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc)，确认该问题尚未被报告过或已得到解决。

在创建新问题时，添加一个简短且有意义的标题和清晰的描述。尽可能多地添加相关信息，并且如果可能的话，附上一个测试用例。

[new-issue]:
  https://github.com/open-telemetry/opentelemetry.io/issues/new/choose
