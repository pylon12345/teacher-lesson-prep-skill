# 教师备课 SKILL（teacher-lesson-prep-skill）

一个给学校老师用的 AI 备课 Skill。输入学科、年级、课题，生成符合新课标、能直接上课的教学设计。

**它会先读你自己的备课知识库**——你的教学风格、班级学情、教材原文、以前的教案、反思和评课意见——所以越用越像你自己备的课。

适用于小学、初中、高中各学科。

## 能做什么

**日常备课**
- 生成完整教案：课标要求、教材分析、学情分析、教学目标、重难点、教学过程、板书、作业、反思
- 按核心素养写教学目标
- 设计分层作业（基础 / 提高 / 拓展）
- 交付前自检（时间分配、目标与环节对应等）

**优质课（赛课 / 公开课）**
- 对照评分标准检查教学设计
- 试讲逐字稿：导入语、过渡语、提问原话、学生回答预设与应对
- 磨课：把评课意见发过来，逐条处理并出新版本（v1 → v2 → …）
- 说课稿

**个人知识库**
- 备课前自动读取你的档案、班级学情、历史教案、反思和评课意见
- 备完课经你同意后存回知识库，下次接着用

## 安装（Claude Code）

```bash
git clone https://github.com/pylon12345/teacher-lesson-prep-skill.git ~/.claude/skills/teacher-lesson-prep
```

安装后，在对话里说「帮我备一节课」或「准备一节优质课」即可使用。

## 建立你的知识库

第一次使用时，Skill 会问你要不要建知识库。也可以手动建：

```bash
cp -r ~/.claude/skills/teacher-lesson-prep/kb-template ~/备课知识库
```

然后先填 `~/备课知识库/00-我的档案.md`，其他资料（Word、PDF、Markdown 都行）往对应文件夹里丢就可以。

知识库放在 Skill 目录之外，更新 Skill 不会影响你的资料。

## 目录结构

```
SKILL.md                         Skill 主文件
references/
  knowledge-base.md              知识库结构、检索和存档规则
  quality-lesson.md              优质课流程与评价维度
  objective-verbs.md             教学目标行为动词
templates/
  lesson-plan.md                 教学设计模板
  lecture-script.md              试讲逐字稿模板
  polish-log.md                  磨课记录模板
  talk-script.md                 说课稿模板
kb-template/                     知识库空白模板
```

## 路线图

- [x] 老师个人知识库
- [x] 优质课模式（逐字稿、磨课、说课稿）
- [ ] 大单元教学设计
- [ ] 课件（PPT）大纲生成
- [ ] 各学科专用模板（语文、数学、英语、理化生……）
- [ ] 试卷与课堂练习生成

## License

MIT
