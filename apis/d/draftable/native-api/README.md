# Draftable: Native API Reference

A consolidated summary of Draftable's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://api.draftable.com
- **OpenAPI specification:** https://api.draftable.com/api-explorer/spec
- **API base URL:** `https://api.draftable.com/v1`

## Authentication

### API Key

Use your Draftable auth token and account ID to connect.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your Draftable account ID, used for viewer URLs and signed links.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.draftable.com/reference/authentication)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comparison](actions/create-comparison.md) | `POST /comparisons` | [docs](https://api.draftable.com/reference/creating-comparisons) |
| [Delete Comparison](actions/delete-comparison.md) | `DELETE /comparisons/{{identifier}}` | [docs](https://api.draftable.com/reference/comparison-lifecycle) |
| [Export Comparison as PDF](actions/export-comparison-as-pdf.md) | `POST /exports` | [docs](https://api.draftable.com/reference/exporting-comparisons) |
| [Get Comparison](actions/get-comparison.md) | `GET /comparisons/{{identifier}}` | [docs](https://api.draftable.com/reference/comparison-lifecycle) |
| [Get Export](actions/get-export.md) | `GET /exports/{{identifier}}` | [docs](https://api.draftable.com/reference/exporting-comparisons) |
| [List Comparisons](actions/list-comparisons.md) | `GET /comparisons` | [docs](https://api.draftable.com/reference/comparison-lifecycle) |
