# PoetryDB: Native API Reference

A consolidated summary of PoetryDB's API configuration and 6 documented operations.

- **API base URL:** `https://poetrydb.org`

## Authentication

### No authentication

This API does not require request authentication.

[Official authentication documentation](https://poetrydb.org/index.html)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Poems by Author](actions/get-poems-by-author.md) | `GET /author/:author` | [docs](https://poetrydb.org/index.html) |
| [Get Poems by Title](actions/get-poems-by-title.md) | `GET /title/:title` | [docs](https://poetrydb.org/index.html) |
| [Get Random Poem](actions/get-random-poem.md) | `GET /random` | [docs](https://poetrydb.org/index.html) |
| [Get Random Poems](actions/get-random-poems.md) | `GET /random/:count` | [docs](https://poetrydb.org/index.html) |
| [List Authors](actions/list-authors.md) | `GET /author` | [docs](https://poetrydb.org/index.html) |
| [List Titles](actions/list-titles.md) | `GET /title` | [docs](https://poetrydb.org/index.html) |
