# Repolex Knowledge Graph of zopefoundation/zope.deferredimport

RDF knowledge graph data for [zopefoundation/zope.deferredimport](https://github.com/zopefoundation/zope.deferredimport), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.deferredimport
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 89517da3bdaa546e81d7e2da01368554b8eb1640
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 89517da3bdaa546e81d7e2da01368554b8eb1640
│           └── chunk-001.nq.gz
├── blob
│   ├── 120923f39ab5607448c6e11d6903887f10b1960e.nq.gz
│   ├── 15eaecc5f4ed887b2c173b1868cdb8a44c4138cc.nq.gz
│   ├── 2276e54471ca6a549746af7a214b8778acc6857e.nq.gz
│   ├── 2596a596db536ea35996d5d7cabb3da57d8bb7d0.nq.gz
│   ├── 415a0447de8cf48c738129d27ab1995dddc99880.nq.gz
│   ├── 41fc0c7a837f14347232e53adb08740dc6815057.nq.gz
│   ├── 4734e9ca55a5a1885416bdd8551887be2af4d4bc.nq.gz
│   ├── 52baa1532dda8f90a66056da855543c138264d90.nq.gz
│   ├── 56938e5ff1dfa08358dc12435c7a10fc7ecef965.nq.gz
│   ├── 56fecdb72a75c4118ba880431beb7a936ff2cef0.nq.gz
│   ├── 5e5874a6850916406663f9b82e750016868ab60b.nq.gz
│   ├── 6ccbe251aded4cb9cb22291f86ea11d3c1bdedd7.nq.gz
│   ├── 6fc09f50e655753e0d5b3836874094472c78d2f3.nq.gz
│   ├── 75a00587a600bac5534022941ee3a508777536d5.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 7c226106301abb43c6056824e806ae2dc00df6e1.nq.gz
│   ├── 7e3bf1174c71b572cec45187fef401b10acdbe15.nq.gz
│   ├── 7fad3e12a9a962b38a4e4f16cac3eead853b8418.nq.gz
│   ├── 874c8027c0fb2fa64fbf6aadb34a57d3f89c40e9.nq.gz
│   ├── 897007e6b0c202d2a19e09c5d7a21d810dbeee7e.nq.gz
│   ├── 8a1cde635fcfe005cc4438d504940505395236a7.nq.gz
│   ├── 8e7ad2ba51a25eb579a49f1003c1274b03bc1e2a.nq.gz
│   ├── a2cb8aee83b0bf54be939f133ab07fcf4b7cc90c.nq.gz
│   ├── a5b240514e9e04183919bddb8852bdd2e5773151.nq.gz
│   ├── aa8267071cbd8cef52b0ed1d95eba94bbcbd7033.nq.gz
│   ├── c1df359cd22d27b3a392010d622a1ce82556da7f.nq.gz
│   ├── c4774639e8873204ccde96b62362276df4795dea.nq.gz
│   ├── c634bd6257977ab9c6d5de4c242f1f303d0ed4e8.nq.gz
│   ├── c7cbbfe7e6b271ade1979f1e2e76c240084c7c16.nq.gz
│   ├── ca517f4eb0cec1c691c0c2b54cd5eb85e906f11b.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e4b867329e05886a4818f86b117fca2102bc84bf.nq.gz
│   ├── e526341d00df7e127c9e3d8b8ebff20e8c8b05a3.nq.gz
│   ├── ec489cca75e78abb74642a1d7792b72d4aeefa04.nq.gz
│   ├── f6f8478c59c387edbc2b7236a87f5a0fa949fb59.nq.gz
│   └── f81cabf053fb4487bb3496afbc276556076bc3f2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 89517da3bdaa546e81d7e2da01368554b8eb1640.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 44 files
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

[zopefoundation/zope.deferredimport](https://github.com/zopefoundation/zope.deferredimport)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
