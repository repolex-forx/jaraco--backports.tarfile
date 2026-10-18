# Repolex Knowledge Graph of jaraco/backports.tarfile

RDF knowledge graph data for [jaraco/backports.tarfile](https://github.com/jaraco/backports.tarfile), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/backports.tarfile
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6ff4300ff5eda255c6aee636f1800dffde9ad066
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6ff4300ff5eda255c6aee636f1800dffde9ad066
│           └── chunk-001.nq.gz
├── blob
│   ├── 07a89cc53bb9053f962014ca1cd555770a2418b0.nq.gz
│   ├── 0d1f7edf5dc6343538563a8caa7de6829752c4f9.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 23fd2168ae57388e73dee24451e82cad5840ec86.nq.gz
│   ├── 2cf7d597659d3a683a4b6bd8c4fea88907508cdc.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 31fc0b2021f7782b676314c9ac44900279798022.nq.gz
│   ├── 40c053fb7f8fc32b24d0b769932580692e05e28d.nq.gz
│   ├── 512fa149e6cfda08642420ce6e17cabe02893c92.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 5d0a528e8a25beb2cbf86518339300d89c3caad8.nq.gz
│   ├── 6b2368309d73512b360ceebdc9f2bd99e6071392.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 994fec2ffd0247d1b255d4546799db906815cbce.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── 9d1a54f314ec5eecb2845e4a35f4166abe56b538.nq.gz
│   ├── ac21d7a1edd2ca1177f071465ca141ab405b1927.nq.gz
│   ├── ad42b101e91d843329d813740b8333d743a512cd.nq.gz
│   ├── b8237251964983f54ed1966297e887636cd0c5f4.nq.gz
│   ├── bb9345373e9701b01f16b70844445dfe1863abc6.nq.gz
│   ├── c4f5a58a946de660c57f56050d4e7f35b8d5e2fe.nq.gz
│   ├── c55b40c33163bbfb731652a2764e8c3fb353da90.nq.gz
│   ├── cc0c66ec9deec022463319be89a9d7a4f596de65.nq.gz
│   ├── daf55090862ae43283b6552073549ac3ab2ad50a.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e17105b6175a3039c6a8925e37a9515f0e28fc7a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   ├── fb25fde5794fa5d0bdf98501e7f8f719163e4f5a.nq.gz
│   └── ff6d291ee4e6c536e3bd9c372de39a513e4b11b2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6ff4300ff5eda255c6aee636f1800dffde9ad066.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 43 files
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

[jaraco/backports.tarfile](https://github.com/jaraco/backports.tarfile)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
