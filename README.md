# Repolex Knowledge Graph of pytest-dev/pytest-randomly

RDF knowledge graph data for [pytest-dev/pytest-randomly](https://github.com/pytest-dev/pytest-randomly), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-randomly
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 35dcf0a5df9f41d57a44cc01e1eec594af23ff89
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 35dcf0a5df9f41d57a44cc01e1eec594af23ff89
│           └── chunk-001.nq.gz
├── blob
│   ├── 11bcdd765a9777521b751cdd1df8982c46d9f1bc.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 36607e5aaecd349f4e6a689806a6bb388c66d4fc.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 3d58272fe72875d0be4561fd9ba58b000e62cf27.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 438d629c3ce988e3afffa71110b9660853d38549.nq.gz
│   ├── 6058b59e75b39099c8e47476f2b7d0bf544c330e.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 8da717565c14e8e8059e29aeceb019e124fe3ce4.nq.gz
│   ├── 96a0dd6023b6e2826cc0a07b972e511a89aea275.nq.gz
│   ├── b9b142e7fdd9016ef5677ec4d250f32cbf2701cf.nq.gz
│   ├── cbe1d62d353e1468867c1ac699e6a64411e200d3.nq.gz
│   ├── d3640c4e408bb3995b66fbe47cc7a269694daf99.nq.gz
│   ├── db8216c6d9b966208a92d3216b82a87c5dd2f758.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0a2abfa16717167b289159a2f38a41fde8a3457.nq.gz
│   └── f9f724a06ef9fa37d3424168455fbcf0bd836cf5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 35dcf0a5df9f41d57a44cc01e1eec594af23ff89.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[pytest-dev/pytest-randomly](https://github.com/pytest-dev/pytest-randomly)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
