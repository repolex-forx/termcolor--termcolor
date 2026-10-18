# Repolex Knowledge Graph of termcolor/termcolor

RDF knowledge graph data for [termcolor/termcolor](https://github.com/termcolor/termcolor), parsed by [repolex](https://repolex.ai).

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
rlex download termcolor/termcolor
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c7d0b8e8a42f417ec0c07fd846138b0a19b24d36
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c7d0b8e8a42f417ec0c07fd846138b0a19b24d36
│           └── chunk-001.nq.gz
├── blob
│   ├── 19bcb946ff4e22aaec8018ab56e90c7ef28e3b8e.nq.gz
│   ├── 23d593ed13ed37852dadb944cacba1a934cf39e0.nq.gz
│   ├── 2e37f36b089fd107950602fcddd0767c9a4a370d.nq.gz
│   ├── 338524ca5bc526ca2336582797e6db73ef1bccb8.nq.gz
│   ├── 356a7f6228533b964e3498225a947a56549ba146.nq.gz
│   ├── 462e6dfeccc67afd2c68a13b0953cbc0573bd8d1.nq.gz
│   ├── 4a0524332d379e79ce7362d29042685d2e65e965.nq.gz
│   ├── 5072ae65b57c03fa1aa12e769d3f86ef9f2234e0.nq.gz
│   ├── 522b02158d35478b46bf29fa67654f6ece545514.nq.gz
│   ├── 529c354324a8e89420e1644a67ac51700a42c1d9.nq.gz
│   ├── 54367daeb4deff4d1d069904fa49783d8c6d7dca.nq.gz
│   ├── 66df94fef7e189ebfea06a56d602e14779500671.nq.gz
│   ├── 66f2260797d81681e4b6bb954e68017308f8326c.nq.gz
│   ├── 69909cba69f453eb5c70d9e00c3e8de58c086db1.nq.gz
│   ├── 6d86f29076b06a3b91844fda41860199d9f30c52.nq.gz
│   ├── 7d285c603c22c674ef753686f54bec175606059e.nq.gz
│   ├── 8bcf6461599ec56769b3a5747041a5ac73adcd2e.nq.gz
│   ├── 9a38e3bc389c0a31f4de405a687725ffdd671c2b.nq.gz
│   ├── 9d3236aa6620be0c6fc1499a06aeff3b6d0d7896.nq.gz
│   ├── a9058e36bd8cbe656c693129316399bf5920d1cf.nq.gz
│   ├── c046c06f6b26aa0bd8c0c8ff320582194d9176e2.nq.gz
│   ├── d0b79705c354418108635b67e17ee15443a4a130.nq.gz
│   ├── d6a6ad9be2fe28206af3b3140b83f1fa9e585555.nq.gz
│   ├── daf7cf185852a93d31334ca60d386baf390fe124.nq.gz
│   ├── dfa3bef8335f9959658de3d88d7a3b7b43a01778.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f7f3616bd9c8f322a86ea89947c9cca0c141dabd.nq.gz
│   └── f94c2e5f742942aede54ece316c3ba03eafd5a38.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c7d0b8e8a42f417ec0c07fd846138b0a19b24d36.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[termcolor/termcolor](https://github.com/termcolor/termcolor)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
