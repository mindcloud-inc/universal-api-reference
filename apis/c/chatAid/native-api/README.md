# Chat Aid: Native API Reference

A consolidated summary of Chat Aid's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.chataid.com/api-guide/
- **API base URL:** `https://api.chataid.com`

## Authentication

### API Key

Use a Chat Aid Custom APIs key in the Authorization header without a Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.chataid.com/api-guide/)

## API conventions

Responses from this API use JSON. The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Custom Source](actions/delete-custom-source.md) | `DELETE /external/sources/custom/:id` | [docs](https://docs.chataid.com/api-guide/custom-sources) |
| [Delete Custom Sources by IDs](actions/delete-custom-sources-by-ids.md) | `DELETE /external/sources/custom` | [docs](https://docs.chataid.com/api-guide/custom-sources) |
| [Get Completion Result](actions/get-completion-result.md) | `GET /chat/completions/custom/:promptId` | [docs](https://docs.chataid.com/api-guide/completion) |
| [Get Custom Source](actions/get-custom-source.md) | `GET /external/sources/custom/:id` | [docs](https://docs.chataid.com/api-guide/custom-sources) |
| [List Custom Sources](actions/list-custom-sources.md) | `GET /external/sources/custom` | [docs](https://docs.chataid.com/api-guide/custom-sources) |
| [Submit Question](actions/submit-question.md) | `POST /chat/completions/custom` | [docs](https://docs.chataid.com/api-guide/completion) |
| [Upload Custom Sources](actions/upload-custom-sources.md) | `POST /external/sources/custom` | [docs](https://docs.chataid.com/api-guide/custom-sources) |
