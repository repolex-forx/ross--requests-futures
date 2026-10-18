# Repolex Knowledge Graph of ross/requests-futures

RDF knowledge graph data for [ross/requests-futures](https://github.com/ross/requests-futures), parsed by [repolex](https://repolex.ai).

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
rlex download ross/requests-futures
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 73f85fbe0f5ac7599850bddec7108bd57a6249cc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 73f85fbe0f5ac7599850bddec7108bd57a6249cc
│           └── chunk-001.nq.gz
├── blob
│   ├── 02e3e7ad74a2e2302d81f7194649cecd59d4d9a9.nq.gz
│   ├── 036a736393c4894741f021f1fbb752de8702ed10.nq.gz
│   ├── 0bea4de3f9ed17ec0e90ac54d9fc23cbd8d19bc4.nq.gz
│   ├── 1c209e4a19d2bdb736daaf1c82807112612e28d3.nq.gz
│   ├── 2091fae5f99aedbd87b4a9e28b7f59867b2ae994.nq.gz
│   ├── 2138bcd1b75fbedf6691861a28af36efc4f8ac72.nq.gz
│   ├── 282eb1bd6f537d6cce3ed4e5dbed163396dd23cd.nq.gz
│   ├── 2a2a0c62888507c7bb086c6e68ae7acf715b5a7e.nq.gz
│   ├── 2b9d186ed9238433820d4ae05a0dc3e3f9eab536.nq.gz
│   ├── 2d08d87d0f06c06ec41436f6d594765649f6132e.nq.gz
│   ├── 36cfea376b026f2e6d3a6a0eea4924a10c5882a5.nq.gz
│   ├── 3949fddf61600ce88863758851be569035517a1f.nq.gz
│   ├── 452321dc7f9299c857220368a5173c72f5413405.nq.gz
│   ├── 45747337775e8f7b249802e02d88b47120282c1a.nq.gz
│   ├── 4a9d8fba70572836c01b9586e56b6ebabafb0cda.nq.gz
│   ├── 52828878459186ebe9cc774c00115343f30ae129.nq.gz
│   ├── 529138ddb62c67bbed446edcf998f3ef888e3ee4.nq.gz
│   ├── 56907a318d29f51d47ccaec7a639d3e541c8ca1d.nq.gz
│   ├── 59e29ec51dbe8155f4c854a716e7f566e6ad58d5.nq.gz
│   ├── 5b9553554c84fe1ab857d97bd31a1ee9defeebd0.nq.gz
│   ├── 5d2ad5ed4612643a07353eed3025aa49be55346f.nq.gz
│   ├── 6a7d5f1597a4a7ee3a0fb7af197a22bfa3710ac5.nq.gz
│   ├── 6afb02b0b4baf5a283ecf855da827405c87000b2.nq.gz
│   ├── 86d6fce34d1fef2254a8c0e4af187c97faf32c93.nq.gz
│   ├── 8995c231d537c782600b7ae820f97d901c33d58b.nq.gz
│   ├── 90a4e60b5d67a347a4af52b1ac49e8874704dfc5.nq.gz
│   ├── 920c82a5e0b2139d9cbe10c87121bc691974b7fc.nq.gz
│   ├── 995cd91b60e9510e95648851169df1dc2eae61c7.nq.gz
│   ├── 9dc1d064091a5f3b12efbbeec5c6fc52c79cd427.nq.gz
│   ├── c092dca8534c36a5c946ff9eaa259f3daa266dff.nq.gz
│   ├── cbaed4555aa149f7dacb0933e9a7203784948ba9.nq.gz
│   ├── cbd795498027af47cae0f8d2bc8e63ede3bbb3ed.nq.gz
│   ├── d0a1d319f7a47ded15b5cf32c59506f24d78b66c.nq.gz
│   ├── d8968f6ee32b3c7cf93d73ece28f839a9fbe4ea3.nq.gz
│   ├── d953d044c1833876eb1036ca592d0a6786d4be84.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e94eaccdc514f913e93d71c1f16c26ee2592468b.nq.gz
│   └── fd497d0388425e20a45fea6c05e5dc4c7f5bd3f9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 73f85fbe0f5ac7599850bddec7108bd57a6249cc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[ross/requests-futures](https://github.com/ross/requests-futures)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
