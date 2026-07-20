# DigiParser: Native API Reference

A consolidated summary of DigiParser's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.digiparser.com/docs/api
- **API base URL:** `https://app.digiparser.com`

## Authentication

### API Key

Authenticate DigiParser API requests with an API key from Team Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.digiparser.com/docs/api/authentication)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Documents](actions/delete-documents.md) | `POST /api/v1/process/:parserId/documents/delete` | [docs](https://www.digiparser.com/docs/api/deleteDocuments) |
| [Get Document Data](actions/get-document-data.md) | `GET /api/v1/process/:parserId/files/data` | [docs](https://www.digiparser.com/docs/api/getDocumentData) |
| [List Parsers](actions/list-parsers.md) | `GET /v1/parsers` | [docs](https://www.digiparser.com/docs/api/authentication) |
| [Reprocess Document](actions/reprocess-document.md) | `POST /api/v1/process/:parserId/reprocess` | [docs](https://www.digiparser.com/docs/api/reprocessDocument) |
| [Upload via URL](actions/upload-via-url.md) | `POST /api/v1/process/:parserId/urls` | [docs](https://www.digiparser.com/docs/api/uploadDocumentUrls) |
