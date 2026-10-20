# Repolex Knowledge Graph of scrapy/form2request

RDF knowledge graph data for [scrapy/form2request](https://github.com/scrapy/form2request), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy/form2request
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a251597d9fa44cbd03736ec1da37f85593dfe820
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a251597d9fa44cbd03736ec1da37f85593dfe820
│           └── chunk-001.nq.gz
├── blob
│   ├── 0af0a659c5e6580383b937896736b36626672d3f.nq.gz
│   ├── 17eb4c41ccaf03ed912be91d3a46d1e480cf003f.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 291074a136cd594ceaf5ce8d772a157f05dbad2e.nq.gz
│   ├── 3772ae921bb7988c0cc79233dce080f345249e19.nq.gz
│   ├── 45718a56a6601b90b90383dbe20b771a23f46445.nq.gz
│   ├── 4842e6bbae036627ba93a795824ecb1af6cdc880.nq.gz
│   ├── 574bfb83f6960c3d5721cb131241a270ffc662f1.nq.gz
│   ├── 623d48cfa6b6f2ba551dde2435254ed5a1b63862.nq.gz
│   ├── 637508e3edb003d7568aa966da6684cf2fa49e50.nq.gz
│   ├── 6bffc658780e3dc910b72912d570398fca81be42.nq.gz
│   ├── 6ffac303d90e714a9cc4e1d52102444eab194a93.nq.gz
│   ├── 7c53e9c7705c4f4bb503f9a800c73f91583ffb6d.nq.gz
│   ├── 7e5a60616e7db35f236d76cb0bf52b81c22f7b1b.nq.gz
│   ├── 800e2b36320098aa25c931c11d6e12103fdd10f7.nq.gz
│   ├── 9ce11036cb169b458435a7ecdb186f52b71530aa.nq.gz
│   ├── bdd2a951b7dd84a9e71e0477e661e0f94d42d820.nq.gz
│   ├── ceffc085163c6ad810a08615482fc0a17fe164ab.nq.gz
│   ├── d6a2c1c8dfb97e7c4798dfe96b54e4352d27fa50.nq.gz
│   ├── db8ae6fd8c35ff5b983bc82b2f3b794224d976d6.nq.gz
│   ├── dd343db665960b1ebc3f02fc838762c0e9296abd.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fc8731d0d978892fba316279397225c125e556e7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a251597d9fa44cbd03736ec1da37f85593dfe820.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[scrapy/form2request](https://github.com/scrapy/form2request)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
