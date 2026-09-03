# 任务路由

先判断使用者此刻要完成什么，再读取最少的相关文件。

| 使用者意图 | 读取的 Skill | 默认去向 |
| --- | --- | --- |
| 记录今天发生的事、感受或身体经验 | `capture-journal` | `journals/` |
| 保存文章、书、播客、课程或对话 | `capture-note` | `notes/` |
| 主动发现一个陌生领域的输入 | `bubble-breaker` | 先留在对话中；完成后进入 `notes/` |
| 回看一周、回应回看问题或寻找可能的输出方向 | `weekly-review` | 回看存入 `reviews/` |
| 已经选定主题，希望先问清楚并持续打磨成文章 | `new-article` | `practices/<输出练习名>/drafts/YYYYMMDD-文章主题.md` |
| 把线索变成可持续行动 | `develop-practice` | `practices/<实践名>/` |

## 组合任务

如果一段材料同时包含外部输入和个人经历：

1. 先区分“外部内容”和“我的回应”。
2. 分别使用 `capture-note` 与 `capture-journal`。
3. 用相对链接把两条记录连接起来。

`weekly-review` 必须同时检查指定范围内的 `journals/` 与 `notes/`，并把回看存入独立的 `reviews/`。不要把回看档案重新当作下一次日记记录或笔记的原始证据。

如果回看中发现可能发展的实践，先展示证据并征得使用者确认，再在 `practices/` 中创建目录。如果发现可能的输出方向，只提供少量候选；使用者选择一个主题并确认继续后，再交给 `new-article`。默认先让使用者自由补充想到的经历，再跨时间检索 `journals/`、`notes/` 与 `reviews/` 中的相关材料，整理主题素材地图；之后才针对空白进入 Grill Me。文章应归入一个已经立项的输出练习，首稿保存到 `practices/<输出练习名>/drafts/YYYYMMDD-文章主题.md`，后续继续更新同一文件；不要把单篇文章主题直接当作 `practices/` 目录名。

如果使用者想打破信息茧房，`bubble-breaker` 负责寻找资源；不要在对方完成之前把推荐当成已经发生的输入。
