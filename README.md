# Repolex Knowledge Graph of pydantic/pydantic-ai-temporal-example

RDF knowledge graph data for [pydantic/pydantic-ai-temporal-example](https://github.com/pydantic/pydantic-ai-temporal-example), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pydantic/pydantic-ai-temporal-example
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ca6194221a3c54a9af2010da1be858ffd8553259
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ca6194221a3c54a9af2010da1be858ffd8553259
│           └── chunk-001.nq.gz
├── blob
│   ├── 1e73087862f22acf3070143b6e468421bb8c54b0.nq.gz
│   ├── 2893f3f7a376eb82f9676dc30ad1dc3d813d0685.nq.gz
│   ├── 2aa0ef9e733f15e4b680ae4b33e13f4f1ff71389.nq.gz
│   ├── 489a277c6c9837447022b230007a003e32e1080f.nq.gz
│   ├── 48b8293bc6150e0e5e22fbc96425c653d35795ee.nq.gz
│   ├── 50acb8e5b4ad9b3935a7ae11d4e06ffe23642409.nq.gz
│   ├── 5444603cf5c7cfd0e04c38c9449cabd477ef1512.nq.gz
│   ├── 5a3e73a8b24f889d02c62b486f14bc016cd24771.nq.gz
│   ├── 73d82d107a36cac0880d2574596ac0da3f3f29b6.nq.gz
│   ├── 7eec9f1d489d60c6966aa30f1eb52e5353218efb.nq.gz
│   ├── a1239eef072027121dc47c3516e1343e92f3a6f8.nq.gz
│   ├── bea7830f99b1c4bf151f5dc2fafc09dfc2d3dc0d.nq.gz
│   ├── bf7f72534aa56bfb0f240e9ee83a9169cf0cad8c.nq.gz
│   ├── c25a48e6fe106be987c2fe29435bb913bd6e295c.nq.gz
│   ├── c3196318b5b44c9ddd8d3599485ea871a478bf67.nq.gz
│   ├── cbbfedaf0ce1d8865da920719a591152807f3076.nq.gz
│   ├── e4fba2183587225f216eeada4c78dfab6b2e65f5.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f8a15fc2f59bb70fed0ea48a150e935c7da3849f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ca6194221a3c54a9af2010da1be858ffd8553259.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 26 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pydantic/pydantic-ai-temporal-example](https://github.com/pydantic/pydantic-ai-temporal-example)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
