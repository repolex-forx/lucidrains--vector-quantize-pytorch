# Repolex Knowledge Graph of lucidrains/vector-quantize-pytorch

RDF knowledge graph data for [lucidrains/vector-quantize-pytorch](https://github.com/lucidrains/vector-quantize-pytorch), parsed by [repolex](https://repolex.ai).

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
rlex download lucidrains/vector-quantize-pytorch
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4103bf2c7be993b6e0ac21d88684818c9880c478
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4103bf2c7be993b6e0ac21d88684818c9880c478
│           └── chunk-001.nq.gz
├── blob
│   ├── 023a8ab4cc23b97c0b900d7a4bc5be1ad705916c.nq.gz
│   ├── 04d7dbb5f67699acd491546f6cbf7c13e88737fb.nq.gz
│   ├── 08caa6c32557f8629c0c023c4e6520eb27bc4b42.nq.gz
│   ├── 0bf49aab3aef7820b169486a13beeb777c78feb9.nq.gz
│   ├── 0d30ad0102c905c3d5c5e214891b4188bf7376a3.nq.gz
│   ├── 15ed416ead38c7adb4687e92b354ac540be511e6.nq.gz
│   ├── 34cd595f2bc19b2ed2b6092d1d51c2ecbdeb1a9e.nq.gz
│   ├── 3cd48cfca8e3e408d69d3321b1c2b307b6da77cf.nq.gz
│   ├── 3e486e3008c1b180bfdb33b9cf109526cee834f4.nq.gz
│   ├── 4bcb166ffd9a434ddbb59d59a4f119472a3c70db.nq.gz
│   ├── 4c82a5dd9248d60064ded8cb163dc2ea7fac4162.nq.gz
│   ├── 4ec6eb39d0c9f9c32e9d3dd17e466a10cb62ffa4.nq.gz
│   ├── 54891e82525a2ff2a9d2958b949a3d16f60a138b.nq.gz
│   ├── 54e76f7b433bd27977b38b3a3744e4cd83fc26ae.nq.gz
│   ├── 6a0e21c60580feaa798d5fe0acb60878256419ff.nq.gz
│   ├── 6f53a0e103b52909786ab92b7aa180d335a28820.nq.gz
│   ├── 7151a3d86dcfcfe18abe4442be251271257c17eb.nq.gz
│   ├── 7b5d606210e788814e4ea984259d9c266b1ffd11.nq.gz
│   ├── 7b68264377b641d51d76abc4ec255e4da3c29462.nq.gz
│   ├── 7ee97ebde5bc36371a7fae634cb7bbe723de9c1c.nq.gz
│   ├── 80649578820f8ff7db6e90f105de628113cc29b7.nq.gz
│   ├── 8848dd77fa9f2b03e3fc40863ac18773d73f5e82.nq.gz
│   ├── 8c419b3110dfbe0dc0a63f0df37377f46b49a642.nq.gz
│   ├── 8e8ea8e114456559461304c42c6176b3dcae661e.nq.gz
│   ├── a317ab183f0922b9f2d6225f4033660967463d94.nq.gz
│   ├── a3fdf6df75182860ba05bd9e57c2f860f06058b0.nq.gz
│   ├── a58375ec609d81109d56d7b5471b02a8a2499b96.nq.gz
│   ├── b189792f2c96bb19ebcd63d94411117ea37d4e04.nq.gz
│   ├── bb9ba6775d2d7164026a62887fe1da58f5401346.nq.gz
│   ├── c55da6a08ddbc626a0bc0ca5da774d1b76d1bf5e.nq.gz
│   ├── c9060e7fbc140db7b49ecdc9297a33ea70e1b9df.nq.gz
│   ├── cad43213602892aadc2290cca7afa74cc9f6af64.nq.gz
│   ├── d22a3427ef9cbc1eb2fbb3c259465b84b6db3095.nq.gz
│   ├── e711260ef73d3b53fbb36370ab6bb4842363ae48.nq.gz
│   ├── e7d506f013590ae9780b7db0cedd7a0b02e988c3.nq.gz
│   ├── e8432e05782d9bad94e2c03c47901947238a4d52.nq.gz
│   ├── f4f4fece070de3f7375561b8f2aae5138a438758.nq.gz
│   └── f6636d6070ac280b925a344164ad41f9925b016b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4103bf2c7be993b6e0ac21d88684818c9880c478.nq.gz
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

[lucidrains/vector-quantize-pytorch](https://github.com/lucidrains/vector-quantize-pytorch)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
