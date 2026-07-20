# ACLU: Native API Reference

A consolidated summary of ACLU's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.thetorturedatabase.org/api
- **API base URL:** `https://www.thetorturedatabase.org/rest`

## Authentication

### No authentication

This API does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://www.thetorturedatabase.org/api)

## API conventions

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Node By NID](actions/get-node-by-nid.md) | `GET /fullnode/retrieve.json` | [docs](https://www.thetorturedatabase.org/api) |
| [List Nodes By Type](actions/list-nodes-by-type.md) | `GET /getnode/retrieve.json` | [docs](https://www.thetorturedatabase.org/api) |
| [Search Nodes](actions/search-nodes.md) | `GET /searchnode/retrieve.json` | [docs](https://www.thetorturedatabase.org/api) |
