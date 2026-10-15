# Repolex Knowledge Graph of jupyter-server/pytest-jupyter

RDF knowledge graph data for [jupyter-server/pytest-jupyter](https://github.com/jupyter-server/pytest-jupyter), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-server/pytest-jupyter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9509dd22d3a29122373d8a5ae134632f10abce21
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9509dd22d3a29122373d8a5ae134632f10abce21
│           └── chunk-001.nq.gz
├── blob
│   ├── 02aa1cd51fc2ba7cc7016db9ebc6cb4fbfbfdae0.nq.gz
│   ├── 0633feb8ed9d5537d04c88d0718006d051b0cd26.nq.gz
│   ├── 16cd55420ae50df8b03fee2e9574c9d008c79d23.nq.gz
│   ├── 1c1a5bbbb3e504e752e2d2d4a47fd3e02fa737ab.nq.gz
│   ├── 1cc4277345532c6b41a50c2f7513635c411f4e0c.nq.gz
│   ├── 396330bb9729d2ec595617aef79fb28600d86bd7.nq.gz
│   ├── 3a9c669557178e70af8143e1ce00c5e2a6e94b5b.nq.gz
│   ├── 434609a71ba1ee3afa37a9bed00618243a882bcc.nq.gz
│   ├── 4d2fa97b31e98b2d25bc2935230061adb26ae964.nq.gz
│   ├── 526d7600a80dc97d9f4244837e332e8a9ed6e65c.nq.gz
│   ├── 5295e776b63d7adfab3ddad99962cc6f81968909.nq.gz
│   ├── 54823a44ec348638bfbfe1c23b7aabd53ef4cb3b.nq.gz
│   ├── 60af4c5f16741c7c2fe17cdd9718ae5f6d56d8a4.nq.gz
│   ├── 79964f9f5da8e4929edddce2c9d7afbecc1726e7.nq.gz
│   ├── 7d5a1dac06680dd819f1e87d880a1e64cc114917.nq.gz
│   ├── 7faeffc91d539a768c105a8bc7f5466e2bbff7a7.nq.gz
│   ├── 8e636a7088218ef67ce5753d8bbfdf7786987e75.nq.gz
│   ├── 8fa37eb1e94ffb0006d2560ea7d59bfe390f6c1c.nq.gz
│   ├── 922152e96a04a242e6fc40f124261d74890617d8.nq.gz
│   ├── 94c9383c894c8b5625eba538fd91307a56e3dc15.nq.gz
│   ├── a2d955a6fad1c04b2f7d075d5a44c4f8b87e4778.nq.gz
│   ├── a70ca828e973dec0fa73807b338971947ef8c407.nq.gz
│   ├── ab851ce9a267f9eb2239e9f5fc9fbf3337323ad8.nq.gz
│   ├── b2d51bcbc26529c92ea5f2a9bf5ee0b5edada28b.nq.gz
│   ├── b2e186c03bca2fc04ac8ae7ba22532690b3d6573.nq.gz
│   ├── cb5b940b0d3bc0852b9e6a68cd867e92d3089b99.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── e1977eec48d15c0990a67b30e7d361e2db89b856.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e85463334bb931d222b0c842e2a4112a11f06a5a.nq.gz
│   ├── eab9c3890ca85da10e9b72f58bdbc4678ab71b3d.nq.gz
│   ├── fe42e8b14c72f30e8218cba5e4dd3fcba11fae30.nq.gz
│   └── fe7c8a36f87d396734be9a9bf60497a803745a5c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9509dd22d3a29122373d8a5ae134632f10abce21.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[jupyter-server/pytest-jupyter](https://github.com/jupyter-server/pytest-jupyter)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
