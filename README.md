# Personal Knowledge Graph Agent

个人知识图谱Agent — 5-Agent协作自动构建与查询个人知识图谱。

## Architecture

```
DocumentParser → EntityExtractor → RelationBuilder → GraphBuilder → QueryAgent
     (4格式)          (4策略)          (3层级)          (3导出)         (6查询)
```

## Features

- **多格式解析**: 支持 Markdown / Python / 纯文本 / JSON 四种格式
- **混合实体抽取**: 关键词匹配 + 正则模式 + 词频统计 + 代码感知四种策略
- **多层级关系推断**: 共现分析 → 模式匹配 → 结构推断三级递进
- **多格式导出**: JSON持久化 + DOT(Graphviz) + Mermaid图表
- **自然语言查询**: 支持6种查询模式 — 详情/邻居/关系/搜索/路径/统计

## Quick Start

```bash
# 构建知识图谱
python main.py build -s ./my_notes -o ./output

# 交互式查询
python main.py query -o ./output

# 单次查询
python main.py ask -o ./output -q "Python相关的概念有哪些？"

# 一站式运行
python main.py run -s ./my_notes -o ./output
```

## Agent Pipeline

| Agent | 职责 | 关键能力 |
|-------|------|---------|
| DocumentParser | 文档解析 | 4种格式解析、section提取、metadata标注 |
| EntityExtractor | 实体抽取 | 4策略混合、8种实体类型、100+关键词库 |
| RelationBuilder | 关系构建 | 3层级推断、12种关系类型、18种模板 |
| GraphBuilder | 图构建 | JSON持久化、DOT/Mermaid导出、连通分量分析 |
| QueryAgent | 智能查询 | 6种查询模式、自然语言理解、结果格式化 |

## Requirements

- Python 3.8+
- No external dependencies (pure Python implementation)
