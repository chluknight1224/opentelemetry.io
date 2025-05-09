---
title: 博客
description: 学习如何提交一篇博客文章。
weight: 30
---

[OpenTelemetry 博客](/blog/) 会发布新功能介绍、社区报告，以及任何与开放遥测社区相关的新闻。
这其中涵盖了终端用户和开发人员。任何人都可以撰写博客文章，阅读以下内容来了解有哪些要求。

## 文档还是博客文章?  {#documentation-or-blog-post}

在撰写博客文章之前，先问问自己，你的内容是否也适合添加到文档中。如果答案是 “是”，那就创建一个新issue或拉取请求（PR），附上你的内容，以便将其添加到文档里。

请注意，OpenTelemetry 网站的维护者和审批者的工作重点是完善该项目的文档，因此对你的博客文章的审核优先级会较低。

## 在提交一篇博客文章之前 {#before-submitting-a-blog-post}

博客文章不应具有商业性质，且应包含广泛适用于 OpenTelemetry 社区的原创内容。博客文章应遵循 [社交媒体指南](https://github.com/open-telemetry/community/blob/main/social-media-guide.md) 中概述的政策。

核实你想要呈现的内容广泛适用于 OpenTelemetry 社区。
合适的内容包括:

- OpenTelemetry 新功能
- OpenTelemetry 项目更新
- 来自各特别兴趣小组的更新内容
- 教程和操作指南
- OpenTelemetry 集成

不合适的内容包括：

- 供应商产品推销

如果你的博客文章符合合适内容的列表，[提出一个问题](https://github.com/open-telemetry/opentelemetry.io/issues/new?title=New%20Blog%20Post:%20%3Ctitle%3E)
附上以下详细信息：

- 博客文章的标题
- 你博客文章的简短描述和大纲
- 如果情况允许， 请列出你博客文章中使用的技术。确保所有技术都是开源的，并且相较于非 CNCF 的项目，优先使用 CNCF 的项目
（例如，使用 Jaeger 进行追踪可视化，使用 Prometheus 进行指标可视化）
- [SIG](https://github.com/open-telemetry/community/) 的名称, 这与这篇博客文章相关。
- 来自该 SIG 的一位赞助商（维护者或审批者）的姓名，这位赞助商将协助审核该拉取请求（PR）。理想情况下，这位赞助商应来自不同的公司。

SIG 通讯的维护人员将进行核实，确保你的博客文章满足所有被接受的要求。如果你在初始问题详情中无法提及 SIG 或赞助商，他们也会指引你联系合适的 SIG, 你可以向该小组寻求赞助支持。
是否有赞助商是可选的，但如果有赞助商，则更有可能使你的博客文章更快地得到审核和批准。

如果你的 issue 包含了所有必要信息，维护人员将确认你可以继续提交博客文章。

## 提交一篇博客文章 {#submit-a-blog-post}

你可以通过 fork 这个仓库并在本地撰写博客文章，或者使用 GitHub UI 来提交一篇博客文章。 在这两种情况下，我们都要求你遵循
[博客文章模板](https://github.com/open-telemetry/opentelemetry.io/tree/main/archetypes/blog.md) 所提供的说明。

### Fork 并在本地撰写 {#fork-and-write-locally}

在你设置好本地 fork 后，你可以使用模板来创建一篇博客文章。请按照以下步骤从模板创建一篇文章：

1. 从存储库的根目录运行以下命令：

   ```sh
   npx hugo new content/en/blog/2024/short-name-for-post.md
   ```

   如果你的文章包含图片或其他资源，请运行以下命令：


   ```sh
   npx hugo new content/en/blog/2024/short-name-for-post/index.md
   ```

1. 编辑你在上一条命令中提供的路径下的 Markdown 文件。 该文件是根据 [archetypes](https://github.com/open-telemetry/opentelemetry.io/tree/main/archetypes/) 目录下的博客文章模板初始化的。

1. 将图片或其他文件等资源放入你创建的文件夹中。

1. 当你的文章准备好后，通过拉取请求来提交它。

### 使用 GitHub UI {#use-the-github-ui}

如果你不想创建一个本地 fork, 你可以使用 GitHub UI 去创建一个新的文章。按照以下步骤使用 UI 添加一篇文章:

1.  前往
    [博客文章模板](https://github.com/open-telemetry/opentelemetry.io/tree/main/archetypes/blog.md)
    然后点击菜单右上角的 “复制原始内容”。

1.  选择
    [创建一个新文件](https://github.com/open-telemetry/opentelemetry.io/new/main).

1.  将你在第一步中复制的模板内容粘贴过来。

1.  命名你的文件，例如
    `content/en/blog/2022/short-name-for-your-blog-post/index.md`.

1.  在 GitHub 中编辑 Markdown 文件。

1.  当你的帖子准备好后，选择**提交更改**，然后按照相应的说明进行操作。

## 发布时间线 {#publication-timeline}

OpenTelemetry 博客并不遵循严格的发布时间安排，这意味着：

- 你的博客文章在获得所有必要的批准后将会被发布。
- 如果有需要，发布时间可以推迟，但维护人员无法保证在某个特定日期或之前发布。
- 某些博客文章（重大公告）具有优先权，可能会先于你的博客文章发布。
