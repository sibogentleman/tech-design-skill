# tech-design

生成用于研发评审的中文技术方案，重点写清实现，包含架构图、关键时序图和核心功能伪代码。

## 特点

- 简练表达：减少背景铺垫，不反复描述通用原则和边界。
- 图文一致：用 Mermaid 展示模块与执行流程，图、正文、代码使用相同的接口和状态名称。
- 实现具体：每项本期核心功能给出输入、输出、分支和核心伪代码。
- 按需裁剪：小项目合并章节，复杂项目补充监控、灰度、迁移、验收与排期。
- 依据清楚：区分现有事实、拟议设计和待确认事项，不虚构验证结果。

## 安装到 Codex

在 Codex 中发送：

```text
使用 $skill-installer 安装这个 skill：
https://github.com/sibogentleman/tech-design-skill/tree/main/skills/tech-design
```

也可以将本仓库的 `skills/tech-design` 目录复制到 `$CODEX_HOME/skills/`；未设置 `CODEX_HOME` 时使用 `~/.codex/skills/`。如果已经安装，请先备份旧目录。

安装后，在下一轮对话中使用 `$tech-design`。

## 使用

```text
使用 $tech-design，根据当前需求和代码生成技术方案，包含架构图、关键时序图和各核心功能伪代码。
```

```text
使用 $tech-design，精简这份现有技术方案，保留有效内容与来源，补齐关键流程和实现伪代码。
```

可以附上需求、仓库位置、现有方案或指定模板。默认输出 Markdown；普通文档生成不依赖飞书、Figma 或外部 CLI。写入飞书等外部平台时，需要当前环境提供相应工具。

## 文件

- [SKILL.md](skills/tech-design/SKILL.md)：生成流程与写作要求。
- [report-format.md](skills/tech-design/references/report-format.md)：可裁剪的报告结构。
- [openai.yaml](skills/tech-design/agents/openai.yaml)：Codex 显示名称与默认提示词。
