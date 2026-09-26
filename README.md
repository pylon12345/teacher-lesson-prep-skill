# 教师备课 SKILL（teacher-lesson-prep-skill）

一个给学校老师用的 AI 备课 Skill。目标不是多产出文档，而是**让老师用更少的时间，上好自己班上的这节课**。

它会先读你自己的备课知识库——教学风格、班级学情、教材原文、以前的教案、反思和评课意见——所以越用越像你自己备的课。

适用于小学、初中、高中各学科。设计方法参考 [AI Product Manager OS](https://github.com/pylon12345/product-manager-os)：先问题再方案、事实和推断分开、允许说不、不越权。

> **当前阶段：验证中。** 还没有真实老师用过。新功能暂停，先找老师试用，见 [product/mvp.md](product/mvp.md)。

## 能做什么

| 模式 | 什么时候用 | 产出 |
|---|---|---|
| 日常备课 | 平时上课、交检查 | 简案（默认）或详案 |
| 优质课 | 赛课、公开课 | 评分对齐表、详案、试讲逐字稿、磨课记录（v1→v2→…）、说课稿 |
| 课后反思 | 上完课 | 反思记录，下次备同一课时自动参考 |
| 知识库 | 建库、存档 | 老师自己的备课资料库 |

它会做到：

- **不编造教材**：教材内容只来自你给的资料；凭记忆写的地方标 `[请核对]`。
- **少问问题**：知识库里有的不问，一次最多问 3 个。
- **会说不**：环节超时、活动为热闹而热闹，会直接指出。
- **不擅自改你的资料**：写入知识库前一定先问你。

## 安装（Claude Code）

```bash
git clone https://github.com/pylon12345/teacher-lesson-prep-skill.git ~/.claude/skills/teacher-lesson-prep
```

安装后，在对话里说「帮我备一节课」或「准备一节优质课」即可使用。

## 建立你的知识库

第一次备完课，Skill 会问你要不要建。也可以手动建：

```bash
cp -r ~/.claude/skills/teacher-lesson-prep/kb-template ~/备课知识库
```

先填 `00-我的档案.md` 和一个班级学情文件就能用。其他资料（Word、PDF、Markdown）往对应文件夹里丢。知识库放在 Skill 目录之外，更新 Skill 不会影响你的资料。

## 目录结构

```
SKILL.md                   主文件：原则、知识库门禁、路由、检查、结尾格式
references/
  mode-daily.md            日常备课
  mode-quality.md          优质课（评分对齐、逐字稿、磨课、说课）
  mode-reflect.md          课后反思
  knowledge-base.md        知识库结构、建库、检索、存档
  quality-lesson.md        优质课流程与评价维度
  objective-verbs.md       教学目标行为动词
templates/                 简案、详案、逐字稿、磨课记录、说课稿
kb-template/               知识库空白模板
tests/cases.md             行为测试用例（人工评估）
product/                   这个 Skill 的产品上下文、问题简报、MVP 计划、决策记录
```

## 路线图

- [x] 日常备课（简案 / 详案）
- [x] 老师个人知识库
- [x] 优质课模式
- [ ] **进行中：找 3～5 位真实老师验证**（见 [product/mvp.md](product/mvp.md)）
- [ ] 确定使用渠道（Claude Code / 网页 / 国内 AI 平台，见 [product/decisions.md](product/decisions.md)）
- 暂停，等验证结果再定：大单元设计、PPT 大纲、分学科模板、出题

## License

MIT
