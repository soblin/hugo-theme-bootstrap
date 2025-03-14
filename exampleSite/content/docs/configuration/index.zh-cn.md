+++
title = "配置"
date = 2021-11-27T19:53:24+08:00
featured = true
comment = true
toc = true
reward = true
pinned = true
categories = [
  "配置"
]
tags = [
]
series = [
  "文档"
]
images = []
weight = 980
aliases = [
  "/zh-cn/posts/configuration"
]
[menu.footer]
  parent = "docs"
  weight = 2
+++

如示例站点所示，我们使用 [Configuration Directory](https://gohugo.io/getting-started/configuration/#configuration-目录) 为了维护更简单的组织和特定于环境的设置，它在多语言站点上特别有用。

<!--more-->

## 站点配置

> 站点配置文件默认为 `config/_default/config.toml`。

| 名称 | 类型 | 默认值 | 说明
|---|:-:|:-:|---
| `title` | String | - | 站点标题
| `baseURL` | String | - | 站点 URL
| `copyright` | String | - | 站点版权。`{year}` 占位符会被替换为当前年份。
| `defaultContentLanguage` | String | `en` |
| `defaultContentLanguageInSubdir` | Boolean | `false` |
| `paginate` | Integer | `10` |
| `paginatePath` | String | `page` |
| `enableRobotsTXT` | Boolean | `true` |
| `disqusShortname` | String | - | [Disqus]({{< ref "/docs/widgets/comments#disqus" >}}) shortname。
| `googleAnalytics` | String | - | Google Analytics.
| `social` | Object | - | [社交链接]({{< ref "/docs/widgets/social-links" >}})。
| `author` | Object | - | [作者小部件]({{< ref "/docs/widgets/author" >}})。

请参阅 [All Configuration Settings](https://gohugo.io/getting-started/configuration/#all-configuration-settings)。

## 站点参数

> 站点参数文件默认为 `config/_default/params.toml`。

| 名称 | 类型 | 默认值 | 说明
|---|:-:|:-:|---
| **Page** 
| `mainSections` | Array | `["posts"]` | 主要的 sections
| `titleCase` | Boolean | `false` | 标题首字母是否大写
| `titleSeparator` | String | `-` | 标题分隔符
| `backgroundImage` | Array | `[]` | 背景图，如：`['/images/bg.png']`, `['/images/bg-light.png', '/images/bg-dark.png']`。
| `comment` | Boolean | `true` | 是否开启评论
| `toc` | Boolean | `true` | 是否开启目录
| `tocPosition` | String | `sidebar` | 可选值：`sidebar` 和 `content`，仅作用于 `post` 布局。
| `tocWordCount` | Integer | `280` | 仅当文章的字数超过此值时，才会显示目录。
| `breadcrumb` | Boolean | `true` | 是否开启面包屑导航
| `breadcrumbDivider` | String | `/` | 面包屑导航分隔符
| `dateFormat` | String | `Jan 2, 2006` | 日期格式。 查阅 [Hugo Date and Time Templating Reference](https://gohugo.io/functions/format/#hugo-date-and-time-templating-reference) 以获取详细信息。
| `poweredBy` | Boolean | `true` | 是否显示技术支持。
| `readingTime` | Boolean | `true` | 是否显示阅读时间
| `postDate` | Boolean | `true` | 是否显示发表日期
| `math` | Boolean | `false` | 是否开启 `math`。
| `diagram` | Boolean | `false` | 是否开启 `diagram`。
| `logo` | String/Boolean | `images/logo.webp` | Logo。设置为 `false` 以禁用 Logo。
| `brand` | String | - | Brand
| `description` | String | - | 站点描述
| `keywords` | String | - | 站点关键词
| `color` | String | - | 颜色风格， `light`，`dark` 或者 dynamic（默认）。 
| `palette` | String | - | 默认配色，清理 Cookie 后生效。
| `palettes` | Array | **ALL** | 可选配色，如需禁用此选项，可将其设为空值 `[]`。
| `featuredPostCount` | Integer/Boolean | `5` | 精选文章数，`false` 则隐藏。
| `recentPostCount` | Integer/Boolean | `5` | 最近文章数，`false` 则隐藏。
| `relatedPostCount` | Integer/Boolean | `5` | 相关文章数，`false` 则隐藏。
| `categoryCount` | Integer/Boolean | `10` | 分类数，`false` 则隐藏。
| `tagCount` | Integer/Boolean | `10` | 标签数，`false` 则隐藏。
| `seriesCount` | Integer/Boolean | `10` | 专栏数，`false` 则隐藏。
| `taxonomyPaginate` | Integer | `10` |
| `taxonomyPostCount` | Integer | `3` | 分类的列表文章数，`false` 则隐藏。
| `taxonomySortingMethod` | String | - | 分类排序方式，默认以字母排序。可选值：`popularity`。
| `countTaxonomyPosts` | Boolean | `false` | 显示分类的文章总数。
| `sidebarTaxonomies` | Array | `["series", "categories", "tags"]` | 侧边栏的分类。
| `fullWidth` | Boolean/Object | `false` | 是否全宽
| `fullWidth.{section}` | Boolean | - | 为特定的 section 定义全宽，如：`posts`, `docs`。
| `fixedHeader` | Boolean | `true` | 是否固定头部
| `reward` | Object | - | [打赏小部件]({{< ref "/docs/widgets/reward" >}})，又称 Buy Me a Coffee 小部件。
| `share` | Object | - | 分享按钮
| `share.addThis` | String | - | [AddThis](https://www.addthis.com) `pubid`。
| `fontSize` | Object | 字体大小 | 注释或删除此参数可以禁用字体大小切换器。
| `fontSize.small` | String | `.9rem` | 小字体
| `fontSize.extraSmall` | String | `.8rem` | 更小的字体
| `fontSize.large` | String | `1.1rem` | 大字体
| `fontSize.extraLarge` | String | `1.2rem` | 更大的字体
| `socialShare` | Boolean | `true` | 启用/禁用内置的分享按钮
| `searchBar` | Boolean | `true` | 启用/禁用搜索栏
| **Archive**
| `archive` | Object | - | [归档]({{< ref "/docs/layouts/archives" >}})。
| `search` | Object | - | [搜索]({{< ref "/docs/layouts/search" >}})。
| **Webmaster Site Verification** 
| `siteVerification` | Object | - |
| `siteVerification.google` | String | - | Google
| `siteVerification.bing` | String | - | Bing
| `siteVerification.baidu` | String | - | 百度
| `siteVerification.baiduUnion` | String | - | 百度联盟
| `siteVerification.so` | String | - | 360
| `siteVerification.sogou` | String | - | 搜狗
| `siteVerification.shenma` | String | - | 神马
| **Analytics** 
| `analytics` | Object | - | Analytics.
| `analytics.baidu` | String | - | 百度统计
| **Others** 
| `googleAdsense` | String | - | Google Adsense。
| `customCSS` | Array | - | 自定义 CSS， 主要用于导入外部。 请查阅[自定义资源](#自定义资源)。
| `customJS` | Array | - | 自定义 JS， 主要用于导入外部 JS。 请查阅[自定义资源](#自定义资源)。
| `utterances` | Object | - | [Utterances]({{< ref "/docs/widgets/comments#utterances" >}}) 配置。
| **Creative Commons License**
| `creativeCommons` | Object | - |
| `creativeCommons.by` | Boolean | `true` | 署名
| `creativeCommons.nc` | Boolean | `true` | 非商业
| `creativeCommons.nd` | Boolean | `true` | 禁止演绎
| `creativeCommons.sa` | Boolean | `true` | 相同方式共享
| **Code Block** 
| `codeBlock` | Object | - | 
| `codeBlock.maxLines` | Integer | `7` | 
| `codeBlock.lineNos` | Boolean | `true` | `true`/`false` 表示默认情况下显示/隐藏行号。
| **Post** 
| `post` | Object | - | 
| `post.excerpt` | String | `Summary` | 可选项：`description`
| `post.excerptMaxLength` | Integer | `320` | 
| `post.copyright` | Boolean | `true` | 是否在每个帖子上显示版权部分
| `post.plainifyExcerpt` | Boolean | `true` | `false` 则格式化摘要为 HTML。
| `post.featuredImage` | Boolean | `false` | 于内容上方显示 Featured 图片。
| `post.numberifyHeadings` | Boolean | `false` | 是否自动对标题进行编号。
| `post.numberifyHeadingsEndLevel` | Number | `6` | 自动编号的深度。
| `post.numberifyHeadingsSeparator` | String | - | 编号和标题之间的分隔符。
| `post.tocStyleType` | String | `none` | 目录的 `list-style-type` CSS 属性。
| `viewer` | Boolean | true | [图片查看器]({{< ref "docs/image-viewer" >}})
| `pwa` | Object | - | [渐进式 web 应用]({{< ref "/docs/pwa" >}})
| **Sidebar**
| `sidebar` | Object | - |
| `sidebar.fixed` | Boolean | `false` | 固定默认侧边栏。
| **Meta Tag**
| `metaRobots` | String | - | 空字符串表示禁用。
| `contact` | Object | - | [联系表单]({{< ref "docs/layouts/contact-form" >}})
| `pinnedPost` | Boolean | `true` | 开启/禁用文章置顶。
| `pinnedPostCount` | Integer | `1` | 置顶的文章数量。
| `rss` | String/Boolean | `true` | 在社交链接中显示 RSS 链接。`false` 为不显示，`home` 则总是链接到主页。

> 除了 Google 站长工具外，其他搜索引擎站长工具无法与 `hugo --minify` 同时使用，这是因为它们无法识别优化后的元标签。

## 页面参数

> 页面参数位于 [Front Matter](https://gohugo.io/content-management/front-matter/)。


| 名称 | 类型  | 默认值 | 说明
|---|:-:|:-:|---
| **Page** 
| `description` | String | - | 页面描述
| `keywords` | Array | - | 页面关键词
| `comment` | Boolean | `true` | 是否开启评论，如果评论已被全局关闭，该参数无效
| `toc` | Boolean | `true` | 是否开启目录，如果目录已被全局关闭，该参数无效
| `math` | Boolean | `false` | 是否开启 `math`
| `diagram` | Boolean | `false` | 是否开启 `diagram`
| `reward` | Boolean | `true` | 是否开启打赏
| `breadcrumb` | Boolean | `true` | 是否开启面包屑导航
| `readingTime` | Boolean | `true` | 是否显示阅读时间
| `postDate` | Boolean | `true` | 是否显示发表日期
| `copyright` | Boolean | `true` | 是否显示版权部分
| `carousel` | Boolean | `false` | 是否在 Carousel 显示
| **Creative Commons License**
| `creativeCommons` | Object | - |
| `creativeCommons.by` | Boolean | `true` | 署名
| `creativeCommons.nc` | Boolean | `true` | 非商业
| `creativeCommons.nd` | Boolean | `true` | 禁止演绎
| `creativeCommons.sa` | Boolean | `true` | 相同方式共享
| **Meta Tag**
| `metaRobots` | String | - | 空字符串表示禁用。
| `pinned` | Boolean | `false` | 置顶文章。
| `featuredPostCount` | Integer/Boolean | `5` | 精选文章数，`false` 则隐藏。
| `recentPostCount` | Integer/Boolean | `5` | 最近文章数，`false` 则隐藏。
| `relatedPostCount` | Integer/Boolean | `5` | 相关文章数，`false` 则隐藏。
