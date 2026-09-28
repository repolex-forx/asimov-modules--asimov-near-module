# Repolex Knowledge Graph of asimov-modules/asimov-near-module

RDF knowledge graph data for [asimov-modules/asimov-near-module](https://github.com/asimov-modules/asimov-near-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-near-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aa6faf12ceb192a9fc846dda776a79055e5d77c9
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── aa6faf12ceb192a9fc846dda776a79055e5d77c9.nq.gz
│   └── repolex
│       └── aa6faf12ceb192a9fc846dda776a79055e5d77c9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ce7e79e0b4754b41a1ee28ef7687b7c0d572637.nq.gz
│   ├── 0ff564ca87fa7af5cb7c36999927fb4b202fe75c.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 2f2b4f7c1a9627ca068db943352c14f509b84683.nq.gz
│   ├── 316dc596b69e77585cf8d7ae4d9118c18b8e8a2d.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 69ec03175d01e69f30f7d0fb9b2526be641e98a9.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 775b37f2025b0b0c44365b5ed0671d9f24131855.nq.gz
│   ├── 777593d02875e95d9ad2c9a10ae70099be17073e.nq.gz
│   ├── 81340c7e72d5c852585d0faea06985a720d4c2df.nq.gz
│   ├── 963319602ecdd43f40d404f2075ba0a71a742e8d.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── aa5d9a7d241664227d6567a42c78614130523c5e.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c11ff1527460d512f8f6c5f8c75421e7357021d1.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e862e6ebfaf8adbaef5346cb2b94c988b2d67e14.nq.gz
│   ├── ebccad64f215fd96dd2103087c7ce0fd63e87416.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── aa6faf12ceb192a9fc846dda776a79055e5d77c9.nq.gz
├── filetree
│   └── aa6faf12ceb192a9fc846dda776a79055e5d77c9.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 30 files
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

[asimov-modules/asimov-near-module](https://github.com/asimov-modules/asimov-near-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
