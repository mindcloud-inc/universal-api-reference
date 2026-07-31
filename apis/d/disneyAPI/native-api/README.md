# Disney API: Native API Reference

A consolidated summary of Disney API's API configuration and 2 documented operations.

- **API base URL:** `https://api.disneyapi.dev`

## Authentication

### No authentication

This API does not require request authentication.

## Pagination

Use `pageSize` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | `GET /character/:id` | [docs](https://disneyapi.dev/docs/) |
| [List Characters](actions/list-characters.md) | `GET /character` | [docs](https://disneyapi.dev/docs/) |
