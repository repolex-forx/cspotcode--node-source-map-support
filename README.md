# Repolex Knowledge Graph of cspotcode/node-source-map-support

RDF knowledge graph data for [cspotcode/node-source-map-support](https://github.com/cspotcode/node-source-map-support), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download cspotcode/node-source-map-support
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e9079eba66f189b3cf94a234597d9b5f2c5a8fc
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0e9079eba66f189b3cf94a234597d9b5f2c5a8fc.nq.gz
│   └── repolex
│       └── 0e9079eba66f189b3cf94a234597d9b5f2c5a8fc
│           └── chunk-001.nq.gz
├── blob
│   ├── 004e1decb51acdd6192a9c28b190c8255dc5ba5b.nq.gz
│   ├── 063cd7c17c5cd44cefa8d87a956b1e7efb0a4a40.nq.gz
│   ├── 0f0c7311997a370507b1e882167c057c1e27bcfd.nq.gz
│   ├── 10991c08355b5fec69784012e884e714a8d0a8c4.nq.gz
│   ├── 223ce6c01d232327487cd8be52194e35d4ff6603.nq.gz
│   ├── 2a962191079219153835e23bf68a8c5581698629.nq.gz
│   ├── 4d6e5cf3bdda2b267c0fb925950af2c216597d9f.nq.gz
│   ├── 4f68e67d02afc93544e773a769a368754bb14686.nq.gz
│   ├── 5274c81a913348fcf5fcdb23406677e46cb3131f.nq.gz
│   ├── 55e12eaf526e76091a9701f6d8182247c9efe119.nq.gz
│   ├── 57210686c2559c5d3b1aaaa3591b1443fe03eb09.nq.gz
│   ├── 5dfc73ba074d1f3c7b67e59cd7fc45f883c9ee9e.nq.gz
│   ├── 5f57bd9d90c25d907d8b6fa1740082786c739c4b.nq.gz
│   ├── 602230c71c36f1b08254aaa8d358e056a5f2fbc1.nq.gz
│   ├── 6247ca912cb4bcc379aed9b711290dc3d174f915.nq.gz
│   ├── 64ad66aa88fe15610fe0698db4f0cd4956883583.nq.gz
│   ├── 699684db0f8d70effd7036bcddb6fdbbffd655b7.nq.gz
│   ├── 6bc12abb7668141cbb13b49b48a859c62f58c493.nq.gz
│   ├── 782da501459760dd729b76cb0a80358063f70e30.nq.gz
│   ├── 7dabc6cca86c53d92a7411efa15a39c5c4056c56.nq.gz
│   ├── 93e7e2ebe325c1fad5735e890e8c60a72e54ca63.nq.gz
│   ├── a718e76d728926de3e007f8638ef99e3220ebd3a.nq.gz
│   ├── a787e696575a57a7b16eb317aa5401fa663f4c93.nq.gz
│   ├── b4995ec327eb732e6f691550e6e8b38c57a2f3a7.nq.gz
│   ├── d6d42d36657eba7b78a6ba3e0cb9c8c0f8e077f6.nq.gz
│   ├── d8cb9d8d352ed05b79068a6e41a821c1aa60cb42.nq.gz
│   ├── ecc0cdfaa3d152850905b8aac6f96474846afb8d.nq.gz
│   ├── ee9999f6222a1cac960604c539e3cdfb6bd6536a.nq.gz
│   ├── f43ee87642d1c2500de8b5038ef533681b2feb82.nq.gz
│   ├── f6cc8d78c96302781c531ebe1e6d036a5b81b214.nq.gz
│   ├── f73907058bcf54c79201466a277d4ca2e6df3572.nq.gz
│   └── fe28f653eb243a91d433cf116a4c7076ebba482a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0e9079eba66f189b3cf94a234597d9b5f2c5a8fc.nq.gz
├── filetree
│   └── 0e9079eba66f189b3cf94a234597d9b5f2c5a8fc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 42 files
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

## Source repository

[cspotcode/node-source-map-support](https://github.com/cspotcode/node-source-map-support)

---
*Parsed on 2026-04-25 by [repolex](https://repolex.ai)*
