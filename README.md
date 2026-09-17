# Repolex Knowledge Graph of alexbrazier/simple-update-notifier

RDF knowledge graph data for [alexbrazier/simple-update-notifier](https://github.com/alexbrazier/simple-update-notifier), parsed by [repolex](https://repolex.ai).

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
lexq download alexbrazier/simple-update-notifier
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9b8f362f37c73c21fda3e99ae7a369175e0716a3
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9b8f362f37c73c21fda3e99ae7a369175e0716a3.nq.gz
│   └── repolex
│       └── 9b8f362f37c73c21fda3e99ae7a369175e0716a3
│           └── chunk-001.nq.gz
├── blob
│   ├── 00386838f7a1c187dcfa359752396fcb84669c89.nq.gz
│   ├── 081074520c35c347eb7d804f2493447faa7aad5b.nq.gz
│   ├── 10c3beb8c40e33ecb73d4cc1292e33fb9cbd97be.nq.gz
│   ├── 1e0b0c116923cb899cb0ebc49528551dde1f6ab9.nq.gz
│   ├── 217337eaebcfcc4892f5271108c050e7d3920299.nq.gz
│   ├── 2b0d2cfcd7a4d1596e2257c7fe0d73cdf9bb49e4.nq.gz
│   ├── 31d5069f97d3abf90d2c105374c21c44bde35b82.nq.gz
│   ├── 3313ff9ef06fbd931144b6c8c0fb62a57d053b64.nq.gz
│   ├── 49e1cb276993af3991196dca44a43f9f14da17a9.nq.gz
│   ├── 4d710a72e90eba53c3e080174ce488e85608e6d4.nq.gz
│   ├── 6313b56c57848efce05faa7aa7e901ccfc2886ea.nq.gz
│   ├── 666b4663afd69b68b46475f09d771bbd1d5624bc.nq.gz
│   ├── 7145ac2f43189ec3c945d1009df3dfe3d4c92d36.nq.gz
│   ├── 98ffb5a9201cc15e27251e3bbe4f190a422ab0eb.nq.gz
│   ├── 9ab5e047de465f08a64f7b47f26918a07996da9b.nq.gz
│   ├── adc69601bc3ac788bc0ebd8fb43124dc9bd281c3.nq.gz
│   ├── af7ab22cacee30687de862601171a819fd95c782.nq.gz
│   ├── b16e98be434576b40484fb3770477f1f19438bbd.nq.gz
│   ├── b78a42e5aa90f08aa6508eb9243e612b8f7c9040.nq.gz
│   ├── beea512cb4335e5f86fc36f4e895e4ad9044b678.nq.gz
│   ├── c395eb002762d0d4cca2b254b073b33db8b83da4.nq.gz
│   ├── d474e1f9ead19135a390c930e5801f4e6910c0a4.nq.gz
│   ├── dae009d025095a760a44d68ff231a8d062e0182b.nq.gz
│   ├── e11deba0ae1e8694311a9cc792014d727534d0df.nq.gz
│   ├── ec177944638c4be4d4d8cf639d00bab0cc774acc.nq.gz
│   └── ee4c8371afc074e93c8bd48bfe6ba9257c19cbee.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9b8f362f37c73c21fda3e99ae7a369175e0716a3.nq.gz
├── filetree
│   └── 9b8f362f37c73c21fda3e99ae7a369175e0716a3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 36 files
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

[alexbrazier/simple-update-notifier](https://github.com/alexbrazier/simple-update-notifier)

---
*Parsed on 2026-09-17 by [repolex](https://repolex.ai)*
