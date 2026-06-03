# claude-skills

Claude / Cursor Agent Skills 集合。

## 包含的 Skills

| Skill | 目录 | 说明 |
|-------|------|------|
| resume-matcher | `resume-matcher/` | 简历与 JD 六维匹配度评估 |
| image-reading | `image-reading/` | 从 JPG/PNG 图片 OCR 提取文本 |

## 安装到 Cursor

将需要的 Skill 目录复制到项目的 skills 路径，例如：

```bash
# 项目级（推荐）
mkdir -p .cursor/skills
cp -r resume-matcher image-reading .cursor/skills/

# 或全局
mkdir -p ~/.cursor/skills
cp -r resume-matcher image-reading ~/.cursor/skills/
```

Cursor 会递归发现 `SKILL.md`；目录名须与 Skill 内 `name` 字段一致。

## 组合使用

`resume-matcher` 在用户提供图片格式 JD/简历时，会先依赖 `image-reading` 完成 OCR，再进行评分。请同时安装两个 Skill。
