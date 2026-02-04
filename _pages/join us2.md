---
layout: page
profiles:
  - align: left
# 新增：网页头部标题+描述（可选，会在纯文本上方显示）
title: 我的纯文本文档  # 网页的H1主标题，显示在页面顶部
description: 这是一个基于page模板的纯文本展示页面  # 标题下方的描述文字（可选）
# 新增：页面级自定义样式，微调纯文本排版（可选，仅对当前页面生效）
_styles: |
  .post { max-width: 800px; margin: 0 auto; padding: 20px; }  # 内容居中+固定宽度+内边距
  .clearfix p { line-height: 1.8; font-size: 16px; color: #333; }  # 纯文本行高+字体+颜色
  .clearfix h2 { margin: 20px 0 10px; color: #2c3e50; }  # 副标题样式
---

## 纯文本展示示例
这是优化后的纯文本内容，排版更舒适，内容居中显示，
行高、字体大小都做了微调，适合大段纯文本阅读。

### 纯文本段落
大段纯文本直接分段写即可，Markdown的空行会自动转为HTML的<p>标签，
模板会自动渲染，无需额外处理。

**注意**：所有样式仅对当前纯文本页面生效，不会影响站点其他页面。
