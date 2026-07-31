# Cat Facts: Native API Reference

A consolidated summary of Cat Facts's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://catfact.ninja/docs?api-docs.json
- **OpenAPI specification:** https://catfact.ninja/docs?api-docs.json
- **API base URL:** `https://catfact.ninja`

## Authentication

### No authentication

This API does not require request authentication.

[Official authentication documentation](https://catfact.ninja/docs?api-docs.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Fact](actions/get-random-fact.md) | `GET /fact` | [docs](https://catfact.ninja/docs?api-docs.json) |
| [List Breeds](actions/list-breeds.md) | `GET /breeds` | [docs](https://catfact.ninja/docs?api-docs.json) |
| [List Facts](actions/list-facts.md) | `GET /facts` | [docs](https://catfact.ninja/docs?api-docs.json) |
