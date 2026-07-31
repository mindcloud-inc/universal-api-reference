# Cataas: Native API Reference

A consolidated summary of Cataas's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://cataas.com/doc.html
- **API base URL:** `https://cataas.com`

## Authentication

### Public API

This API does not require request authentication.

[Official authentication documentation](https://cataas.com/doc.html)

## Pagination

Use `limit` in the query string to set the page size (default 10; minimum 1). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Cats](actions/count-cats.md) | `GET /api/count` | [docs](https://cataas.com/doc.html) |
| [Get Cat Media By ID](actions/get-cat-media-by-id.md) | `GET /cat/:catId` | [docs](https://cataas.com/doc.html) |
| [Get Cat Media By ID With Text](actions/get-cat-media-by-id-with-text.md) | `GET /cat/:catId/says/:text` | [docs](https://cataas.com/doc.html) |
| [Get Random Cat Media](actions/get-random-cat-media.md) | `GET /cat` | [docs](https://cataas.com/doc.html) |
| [Get Random Cat Media By Tag](actions/get-random-cat-media-by-tag.md) | `GET /cat/:tag` | [docs](https://cataas.com/doc.html) |
| [Get Random Cat Media By Tag With Text](actions/get-random-cat-media-by-tag-with-text.md) | `GET /cat/:tag/says/:text` | [docs](https://cataas.com/doc.html) |
| [Get Random Cat Media With Text](actions/get-random-cat-media-with-text.md) | `GET /cat/says/:text` | [docs](https://cataas.com/doc.html) |
| [List Cat Tags](actions/list-cat-tags.md) | `GET /api/tags` | [docs](https://cataas.com/doc.html) |
| [List Cats](actions/list-cats.md) | `GET /api/cats` | [docs](https://cataas.com/doc.html) |
