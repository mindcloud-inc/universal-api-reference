# Airparser: Native API Reference

A consolidated summary of Airparser's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://help.airparser.com/public-api
- **API base URL:** `https://api.airparser.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.airparser.com/public-api/public-api#authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clone Extraction Schema](actions/clone-extraction-schema.md) | `POST /inboxes/:inbox_id/schema-clone` | [docs](https://help.airparser.com/public-api/public-api) |
| [Create Or Update Extraction Schema](actions/create-or-update-extraction-schema.md) | `POST /inboxes/:inbox_id/schema` | [docs](https://help.airparser.com/public-api/public-api) |
| [Delete Inbox](actions/delete-inbox.md) | `DELETE /inboxes/:inbox_id` | [docs](https://help.airparser.com/public-api/public-api) |
| [Get Extended Document Details](actions/get-extended-document-details.md) | `GET /docs/:document_id/extended` | [docs](https://help.airparser.com/public-api/public-api) |
| [List Documents](actions/list-documents.md) | `GET /inboxes/:inbox_id/docs` | [docs](https://help.airparser.com/public-api/public-api) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inboxes` | [docs](https://help.airparser.com/public-api/public-api) |
| [Parse Document Async](actions/parse-document-async.md) | `POST /inboxes/:inbox_id/upload` | [docs](https://help.airparser.com/public-api/public-api) |
| [Parse Document Sync](actions/parse-document-sync.md) | `POST /inboxes/:inbox_id/upload-sync` | [docs](https://help.airparser.com/public-api/public-api) |
