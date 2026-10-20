# Repolex Knowledge Graph of adamchainz/unittest-parametrize

RDF knowledge graph data for [adamchainz/unittest-parametrize](https://github.com/adamchainz/unittest-parametrize), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/unittest-parametrize
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9bfbdd53e4e4dcee61386e024b1b0f3f7020a373
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9bfbdd53e4e4dcee61386e024b1b0f3f7020a373
│           └── chunk-001.nq.gz
├── blob
│   ├── 01b73e2baf3ddeda681a467beff642f967a3d27a.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 265e401cb9cbc1397fa7ee2418896c45d46287f6.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 30acc83b6797da94e6f047ba88ccfb5b934894ee.nq.gz
│   ├── 36b0a647a68abe1d511a9723a7cad46f9035a552.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 438d629c3ce988e3afffa71110b9660853d38549.nq.gz
│   ├── 4fb7faec2960085d0994a23838947e58b6228aa7.nq.gz
│   ├── 61adbc3a9d5c4890a1131cbeb56c2ea4dc2fae4e.nq.gz
│   ├── 663d6b920407c6318f1222445b39e30e44afa9d3.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 8ed59b02f1bda104b9c62d5f726199c487ba5d07.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── bf2611418f409118ef253d13edddecef6c13f845.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ea55c818091acebfa6ba102d0538182f1ce54f1d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9bfbdd53e4e4dcee61386e024b1b0f3f7020a373.nq.gz
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

[adamchainz/unittest-parametrize](https://github.com/adamchainz/unittest-parametrize)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
