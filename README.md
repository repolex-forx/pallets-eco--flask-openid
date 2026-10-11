# Repolex Knowledge Graph of pallets-eco/flask-openid

RDF knowledge graph data for [pallets-eco/flask-openid](https://github.com/pallets-eco/flask-openid), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-openid
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1eccf8a8a2d0ebd27414e99b9278c8b84d933a80
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1eccf8a8a2d0ebd27414e99b9278c8b84d933a80
│           └── chunk-001.nq.gz
├── blob
│   ├── 068b10477ab9ba2218b049b41aba2b92e7563893.nq.gz
│   ├── 1cca09d9adeffbe92dcbba18b8570a53561d8e7c.nq.gz
│   ├── 1e941d8ca3dfaa2522e04702ac10f2dd8c9cd9f7.nq.gz
│   ├── 2c80f93094e2f91e41ca2920e2c9f7796ad0cf51.nq.gz
│   ├── 3046d526f616b6a2d47ff927fcd6854df785437d.nq.gz
│   ├── 32fa6792ceb5291d7bc06ba5529e895c4ac534a0.nq.gz
│   ├── 444bc6713e3d5e33a8ab2859e058d78a0cd2930e.nq.gz
│   ├── 4ef62ac16c885bad0c62f412302ca8e17cf90fdc.nq.gz
│   ├── 7290e580fd86f456caa8feff9d2b4ef26dddf12e.nq.gz
│   ├── 74d7b571da3b6d2e91d2345870ec3d7d5dde6feb.nq.gz
│   ├── 756cf1b27483f2a945291f3427f06a2692439da4.nq.gz
│   ├── 7f60eed3ae566e275ca626fd5b60fb09cfefe864.nq.gz
│   ├── 9bca27fe9bb3a87f575c2922da56ac7c0f5a9444.nq.gz
│   ├── a925d54610b2d6b29414830d03bc99e2a534d5e9.nq.gz
│   ├── b51ca525b41ec0aac9768ea6ca285e907cfea87e.nq.gz
│   ├── bf7b494fc7044e1395c1c821f2babc309277bf78.nq.gz
│   ├── c5299b5c587ceb472d60e44d6fa0c3f4edea638b.nq.gz
│   ├── ce7954ab12080e1cfb0583669a58267bea008a44.nq.gz
│   └── f14c0a9824c8f6edf347d2f09eea0c389e727575.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1eccf8a8a2d0ebd27414e99b9278c8b84d933a80.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[pallets-eco/flask-openid](https://github.com/pallets-eco/flask-openid)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
