# claude-skills

Claude / Cursor Agent Skills 集合。

## 包含的 Skills

| Skill | 目录 | 说明 |
|-------|------|------|
| resume-matcher | `resume-matcher/` | 简历与 JD 六维匹配度评估（内置 JPG/PNG OCR） |

## 安装到 Cursor

```bash
# 项目级（推荐）
mkdir -p .cursor/skills
cp -r resume-matcher .cursor/skills/

# 或全局
mkdir -p ~/.cursor/skills
cp -r resume-matcher ~/.cursor/skills/
```

Cursor 会递归发现 `SKILL.md`；目录名须与 Skill 内 `name` 字段一致（`resume-matcher`）。

## 说明

- **图片输入**：OCR 已内置，无需单独安装 `image-reading`
- **PDF / Word**：若需自动解析，可另行安装 `pdf-reading`、`docx` Skill，或让用户粘贴文本
