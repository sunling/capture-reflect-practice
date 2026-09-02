# 让记录有下文

**Record. Reflect. Practice.**

这是一个与 AI 协作的个人记录、回看与实践系统，也是 **ChatGPT + GitHub** 路径的仓库模板。它不追求收藏所有信息，而是帮助你完成一个朴素的循环：

> 生活与输入 → Journals & Notes → Weekly Review → Practice → 反馈

仓库里没有作者的私人记录，只有目录结构、使用说明，以及 6 个可以继续修改的仓库内 Skill。你可以把它用于个人记录，也可以在“让记录有下文”工作坊中跟着搭建。

## 开始使用

1. 点击 GitHub 页面右上方的 **Use this template**，创建自己的仓库。
2. 如果要写真实日记，建议把新仓库设为 **Private**。
3. 填写 [PROFILE.md](PROFILE.md)，让 AI 了解你的语言、时区和隐私边界。
4. 阅读 [AGENTS.md](AGENTS.md)，了解仓库协作约定。
5. 按照 [ChatGPT + GitHub 配置指南](refs/chatgpt/README.md)连接 GitHub、设置记录入口，并先完成一条不敏感的测试记录。

如果当前页面没有显示 **Use this template**，仓库所有者需要先在 GitHub 的 **Settings → General → Template repository** 中开启它。

## 目录

```text
.
├── journals/          # 发生在自己身上的事、感受与观察
├── notes/             # 书、文章、播客、对话等外部输入
├── reviews/           # 每次回看的存档，不混入原始 Journals & Notes
├── practices/         # 持续实践，以及正在反复打磨的文章草稿
├── refs/chatgpt/      # ChatGPT Project 与定时任务配置
├── .agents/
│   ├── ORCHESTRATOR.md
│   ├── SOUL.md
│   └── skills/        # AI 可按需读取的仓库内工作流
├── PROFILE.md
└── AGENTS.md
```

## 六个示例 Skill

- [capture-journal](.agents/skills/capture-journal/SKILL.md)：把一段经历整理成 Journal，但不替你编造解释。
- [capture-note](.agents/skills/capture-note/SKILL.md)：保存外部输入，同时区分原内容与你的回应。
- [weekly-review](.agents/skills/weekly-review/SKILL.md)：回看最近七天、保存回看档案、提出问题，并发现少量候选输出方向。
- [new-article](.agents/skills/new-article/SKILL.md)：围绕选定主题跨时间召回相关素材，再用 Grill Me 问清表达并持续更新文章草稿。
- [develop-practice](.agents/skills/develop-practice/SKILL.md)：把有证据的线索发展为可持续的小实践。
- [bubble-breaker](.agents/skills/bubble-breaker/SKILL.md)：每次引入一个陌生而具体的世界输入，完成之后再留下记录。

这些是**仓库内 Skill 示例**，目的是展示如何把工作方法写给 AI。它们不会自动安装成 ChatGPT 或 Codex 的全局 Skill；复制仓库后，你可以按自己的习惯继续修改。

## 什么放在哪里

- 今天发生了什么、我有什么感觉：`journals/`
- 我读到、听到或看到什么：`notes/`
- 一段时间里反复出现了什么、我想继续问什么：`reviews/`
- 某个问题反复出现，且我愿意持续行动：`practices/<实践名>/`
- 已经选定一个主题，准备生成并继续打磨文章：`practices/<输出练习名>/drafts/YYYYMMDD-文章主题.md`
- 只是一个念头，还没有证据：先留在 Journals & Notes，不急着立项

## 与 MCP 复用

这个仓库保存的是记录结构、内容和工作方法，并不绑定某一个 AI 客户端。现在可以由 ChatGPT 通过 GitHub 连接直接读写；以后也可以让 MCP 连接同一个仓库，不需要重新迁移记录。

## 豆包 + 飞书版本

如果希望把记录保存在飞书云盘，并通过豆包智能体使用这些工作流，请使用独立仓库：[record-reflect-practice-doubao-feishu](https://github.com/sunling/record-reflect-practice-doubao-feishu)。

## 隐私提醒

- 不要把密码、身份证件、支付信息、住址等敏感信息写入仓库。
- 公开仓库的 Git 历史会保留曾经提交过的内容；之后删除文件，并不等于历史中的内容自动消失。
- 分享截图或示例前，检查姓名、联系方式、二维码和第三方隐私。
- 本模板不包含作者的私人记录。真实记录是否进入 Git，请由你自己决定。

## 设计原则

- 先记录，再解释。
- 让结构服务生活，不让生活迁就结构。
- 回看存档与原始 Journals & Notes 分开，避免把 AI 的总结再次当成新输入。
- 只有出现重复、行动或反馈时，才把线索升级为 Practice。
- AI 可以帮助整理和追问，但不替你定义经验。

本项目采用 [MIT License](LICENSE)。
