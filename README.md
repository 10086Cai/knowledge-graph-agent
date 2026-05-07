# Personal Knowledge Graph Agent

Personal Knowledge Graph Agent - 5-Agent collaborative automatic construction and query of personal knowledge graph.

## Architecture

DocumentParser -> EntityExtractor -> RelationBuilder -> GraphBuilder -> QueryAgent

## Features

- Multi-format parsing: Markdown / Python / Plain text / JSON
- Hybrid entity extraction: Keyword matching + Regex patterns + Word frequency + Code-aware
- Multi-level relation inference: Co-occurrence analysis -> Pattern matching -> Structure inference
- Multi-format export: JSON persistence + DOT (Graphviz) + Mermaid diagrams
- Natural language query: 6 query modes - Detail / Neighbor / Relation / Search / Path / Statistics

## Quick Start

```
python main.py build -s ./my_notes -o ./output
python main.py query -o ./output
python main.py ask -o ./output -q "What concepts are related to Python?"
python main.py run -s ./my_notes -o ./output
```

## Requirements

- Python 3.8+
- No external dependencies (pure Python implementation)
