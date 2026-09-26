# 教师备课 SKILL（teacher-lesson-prep-skill）

一个给学校老师用的 AI 备课 Skill。输入学科、年级、课题，生成符合新课标、能直接上课的教学设计。

适用于小学、初中、高中各学科。

## 能做什么

- 生成完整教案：课标要求、教材分析、学情分析、教学目标、重难点、教学过程、板书、作业、反思
- 按核心素养写教学目标
- 设计分层作业（基础 / 提高 / 拓展）
- 交付前自检（时间分配、目标与环节对应等）

## 安装（Claude Code）

```bash
git clone https://github.com/pylon12345/teacher-lesson-prep-skill.git ~/.claude/skills/teacher-lesson-prep
```

安装后，在对话里说「帮我备一节课」或输入 `/teacher-lesson-prep` 即可使用。

## 目录结构

```
SKILL.md                     # Skill 主文件
templates/lesson-plan.md     # 教学设计模板
references/objective-verbs.md# 教学目标行为动词
```

## 路线图

- [ ] 大单元教学设计
- [ ] 课件（PPT）大纲生成
- [ ] 各学科专用模板（语文、数学、英语、理化生……）
- [ ] 说课稿 / 公开课稿
- [ ] 试卷与课堂练习生成

## License

MIT
