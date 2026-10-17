# Repolex Knowledge Graph of bastibe/python-soundfile

RDF knowledge graph data for [bastibe/python-soundfile](https://github.com/bastibe/python-soundfile), parsed by [repolex](https://repolex.ai).

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
rlex download bastibe/python-soundfile
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e0f2f49f1c244919a576beb4e27fc860f706e822
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e0f2f49f1c244919a576beb4e27fc860f706e822
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c93f66d9852dfd94d4b8dc6d23fb98ed9006bf2.nq.gz
│   ├── 1a70088c4e509a7ccd9ca3899b6041bcd9df83de.nq.gz
│   ├── 26d9bcc801524342ef0eef64b0526c3ff7a12d7e.nq.gz
│   ├── 2ebf61fcb5c57c1f337ae381861d1c5435137339.nq.gz
│   ├── 2f03786dfc615d279878ca2474c4bfedd41c52ee.nq.gz
│   ├── 37d2de04068d929cc72046b6ccec3c06d3fa4602.nq.gz
│   ├── 46a079b5b672840cd7224d73f605bc4f5b41f436.nq.gz
│   ├── 4a926e411aba81a4fab288183681096b68dbf4ae.nq.gz
│   ├── 5d91fd72404ac73b066e4b34a2ebf2ac8f889e2b.nq.gz
│   ├── 6855f27559c0c69fc3bb2db76c4eb64095154a17.nq.gz
│   ├── 6e64d07aa1b417907fb52b4a87d514385c648e18.nq.gz
│   ├── 7dbd8fb275ebaaf25f71d72c5f0a9044701a5ac7.nq.gz
│   ├── 820643c0ad46f8ca62a8651278a84970741eccf2.nq.gz
│   ├── 89cde3d75c03a4578b7cb991610a22df4430f72c.nq.gz
│   ├── 8b1996dd4d8f4ca126f30a0074a6d41b3a7e9247.nq.gz
│   ├── 8cedbd28836a385c16637510ecfd05c6952547d2.nq.gz
│   ├── 9279494d95e8b7bd6294b8c9aba9e8ac8801eda7.nq.gz
│   ├── 96d376208becc680c001b9dce0f0bf5216cf195f.nq.gz
│   ├── a496a145b0920bf355aea796cc953fdc994a0046.nq.gz
│   ├── b30cc88b007016d2f5e1d7aa5ceb489c0e643300.nq.gz
│   ├── b77ee9e9cb1da79d2fa3b7c20676192b03bbcfaa.nq.gz
│   ├── b9d86cfdbce132d88fb0eb42bd5d50081cc045e0.nq.gz
│   ├── bedfed1b57e55238fb2e597d0fa6b994769ddfd1.nq.gz
│   ├── d5535a85ef5914aecf3ce471b2dd786397f224e8.nq.gz
│   ├── dc13ef764db636a78e62a9dca56eb6269a7480e8.nq.gz
│   ├── dd0e55e4b200bef80f29e32489f899166f254ea1.nq.gz
│   └── f9c8df6fb9288cb9427b531404fa084cfb708b3b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e0f2f49f1c244919a576beb4e27fc860f706e822.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[bastibe/python-soundfile](https://github.com/bastibe/python-soundfile)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
