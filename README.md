# Shawn Skills

本仓库用于集中管理可供 AI 工具安装和加载的技能。技能位于 `skills/` 目录，每个技能都是一个独立目录，并包含入口文件 `SKILL.md`。

## 安装方式

将本仓库克隆到本地后，把需要使用的技能目录复制或链接到 AI 工具支持的技能目录。

### 安装单个技能

```bash
cp -R skills/<skill-name> ~/.agents/skills/
```

示例：

```bash
cp -R skills/state-and-revolution ~/.agents/skills/
```

### 安装全部技能

```bash
cp -R skills/* ~/.agents/skills/
```

如果 AI 工具使用其他技能目录，请将命令中的 `~/.agents/skills/` 替换为对应目录。

## 使用方式

安装后重新启动 AI 工具，或执行该工具提供的技能刷新命令。技能名称以各目录中的 `SKILL.md` 文件的 `name` 字段为准。

例如：

```text
请使用 state-and-revolution 技能分析这个问题。
```

也可以直接描述任务。AI 工具会根据 `SKILL.md` 中的 `description` 判断是否加载对应技能。

## 技能结构

```text
skills/
└── <skill-name>/
    ├── SKILL.md
    ├── chapters/       # 可选：章节资料
    ├── references/     # 可选：参考资料
    └── scripts/        # 可选：辅助脚本
```

## 当前技能

| 技能名称 | 目录 |
| --- | --- |
| `a-man-called-ove` | `skills/a-man-called-ove/` |
| `becoming-yongzheng` | `skills/becoming-yongzheng/` |
| `classical-poetry-in-dark-times` | `skills/classical-poetry-in-dark-times/` |
| `kangxi-governance-and-statecraft` | `skills/kangxi-governance-and-statecraft/` |
| `ming-dynasty-1566` | `skills/ming-dynasty-1566/` |
| `state-and-revolution` | `skills/state-and-revolution/` |
| `steve-jobs-biography` | `skills/steve-jobs-biography/` |
| `tang-crisis-and-reconstruction` | `skills/tang-crisis-and-reconstruction/` |
| `township-politics` | `skills/township-politics/` |
| `zhu-rongji-interviews` | `skills/zhu-rongji-interviews/` |

## 注意事项

- 不要只复制 `SKILL.md`，包含的 `chapters/`、`references/` 和 `scripts/` 等目录也是技能的一部分。
- 技能目录名必须与 `SKILL.md` 中的 `name` 保持一致。
- 修改技能后，重新复制对应目录，或删除旧目录后再安装。
- 安装前确认目标 AI 工具支持 `SKILL.md` 格式及对应的技能目录结构。
