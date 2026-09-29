# Repolex Knowledge Graph of NousResearch/hermes-plugin-honcho

RDF knowledge graph data for [NousResearch/hermes-plugin-honcho](https://github.com/NousResearch/hermes-plugin-honcho), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-plugin-honcho
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 32dfd0ba62ae0e8dad82d55fc81515e8c4a181a9
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 32dfd0ba62ae0e8dad82d55fc81515e8c4a181a9.nq.gz
│   └── repolex
│       └── 32dfd0ba62ae0e8dad82d55fc81515e8c4a181a9
│           └── chunk-001.nq.gz
├── blob
│   ├── 00f2d38d8063d0c6b219c0081e51888063b0c55e.nq.gz
│   ├── 021789fb51213ac89fb50ec415ebff28fb62ce32.nq.gz
│   ├── 05e35c1c8425b62134ca8344d4d30fbf8032ead8.nq.gz
│   ├── 317869d95a442b208bda5b8561cd8ca91e1e7fd1.nq.gz
│   ├── 38a0612c9774ce7b722f45f6d287835d70528ee6.nq.gz
│   ├── 4c418496b4c375678601f53ffda3e204bb91e89b.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 7a6e6e9831d992c21befefed5b78cc577d307fac.nq.gz
│   ├── 878dcd3a959fea1082bd5d81c53d11cd5738c6c0.nq.gz
│   ├── 8ce2e91b0c9fe8f7670757d5bad700ab536ba467.nq.gz
│   ├── 8e05f35f8cbd8e42d35c5d1cadc7348a6d5b0304.nq.gz
│   ├── 9b3c0c22df9a0e4c74063d86676de04be6ee76bc.nq.gz
│   ├── a6442a05a94f11669272ef3978fe8b1f1a819b20.nq.gz
│   ├── beb89f82a0699cf5939c3af49c2583596e12d7ae.nq.gz
│   ├── c6024eddfdd4001167e6342f48835cfb44710e7b.nq.gz
│   ├── c6462ab3a3128ab1ba6fd5fcecbd2522939f8042.nq.gz
│   ├── d10902854338161bb9b41ac3c5e6a29f22e13c12.nq.gz
│   ├── d3a4cd9725c152271d99a2463c959c75da4ac2dc.nq.gz
│   ├── e6000210f0d37f87c91badcda8fe7f4230aa3120.nq.gz
│   ├── eabccda9bf9ca9c02f2e770adc17bbbded23af40.nq.gz
│   ├── f236edaf59621db8094f092a1e08d835e000478c.nq.gz
│   └── ff905429249e9b4169493dbac84ef8f2aed4b9ea.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 32dfd0ba62ae0e8dad82d55fc81515e8c4a181a9.nq.gz
├── filetree
│   └── 32dfd0ba62ae0e8dad82d55fc81515e8c4a181a9.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[NousResearch/hermes-plugin-honcho](https://github.com/NousResearch/hermes-plugin-honcho)

---
*Parsed on 2026-09-29 by [repolex](https://repolex.ai)*
