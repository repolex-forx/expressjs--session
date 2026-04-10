# Repolex Knowledge Graph of expressjs/session

RDF knowledge graph data for [expressjs/session](https://github.com/expressjs/session), parsed by [repolex](https://repolex.ai).

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
lexq download expressjs/session
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c10b2a383841766899f6dcf53c8aff8c7fd3d2e7
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c10b2a383841766899f6dcf53c8aff8c7fd3d2e7.nq.gz
│   └── repolex
│       └── c10b2a383841766899f6dcf53c8aff8c7fd3d2e7
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f13ba6a0958b5d4d539519c1d4b92a4c7993922.nq.gz
│   ├── 11ed686c85d2c5dcf5121cf19f72957705e83867.nq.gz
│   ├── 1333615556105a4860b9ffc24ee5823583518ef3.nq.gz
│   ├── 169262af1eb78108dadab270628049b0bfc59594.nq.gz
│   ├── 1a5093189945e4c433742247e834c7d4626c1f81.nq.gz
│   ├── 1b6fef230925d7afae692ae62e8eb4ed98351838.nq.gz
│   ├── 292b20240e892ff8d34457ea043f8ffade1d8319.nq.gz
│   ├── 36387796a0ef10051a854334f02e5f756b6e5405.nq.gz
│   ├── 3793877e838f7f0f00c72f13580fd17d62cf967f.nq.gz
│   ├── 46fed76376cae71231cb2a5cd3deaf333e2be590.nq.gz
│   ├── 492d67d032cc6e83f4922b884ce44244cca19983.nq.gz
│   ├── 76b1021d09a5774679c815f83d1c9a4bccf21c28.nq.gz
│   ├── 8534ee51dd14485951768f0398d7008d57f84335.nq.gz
│   ├── 8b224fdda3ce469f3191d47a9ebe7021cc242301.nq.gz
│   ├── 8bb5907b153e146a001f39835809839708c9f5a5.nq.gz
│   ├── 9b59ff85cb45b8c60f2e39ac0f79e64f68a9aaee.nq.gz
│   ├── b45dc9a886e20dde82304416ee8e64431f7be2bd.nq.gz
│   ├── b6b9f62ff350066f9e559e0e8452b2eed8754005.nq.gz
│   ├── c58268ad26e98c128bf936c8fd32c63453d23f82.nq.gz
│   ├── cdb36c1b4662559d2880d7a1ae9e65ca7497f47e.nq.gz
│   ├── cfdda07048c7951d1b60e01a43e8b5affaf1f7d6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea676e357d1bd93ea8ff9ff87c27b9abe4b155ba.nq.gz
│   ├── f4c50d76415f435ac3023b7386a8b0a1852938bd.nq.gz
│   ├── fae1a0f13c54f29c4197469d5b7236b2545d4173.nq.gz
│   ├── fba1bd89599834c491d6b3f0fe936ba95890ed2d.nq.gz
│   └── fee7608c60366649115e1a0121336a3c28a087be.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── c10b2a383841766899f6dcf53c8aff8c7fd3d2e7.nq.gz
├── filetree
│   └── c10b2a383841766899f6dcf53c8aff8c7fd3d2e7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 37 files
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

[expressjs/session](https://github.com/expressjs/session)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
