# AlgoDocs: Native API Reference

A consolidated summary of AlgoDocs's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.algodocs.com/
- **API base URL:** `https://api.algodocs.com/v1`

## Authentication

### API Key

Authenticate AlgoDocs API requests with the secret API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api.algodocs.com/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://api.algodocs.com/) |
| [Get Extracted Data of a Single Document](actions/get-extracted-data-of-a-single-document.md) | `GET /extracted_data/:documentId` | [docs](https://api.algodocs.com/#extracted-data) |
| [Get Extracted Data of Multiple Documents](actions/get-extracted-data-of-multiple-documents.md) | `GET /extracted_data/:extractorId` | [docs](https://api.algodocs.com/#extracted_data_multiple_documents) |
| [List Document Data Extractors](actions/list-document-data-extractors.md) | `GET /extractors` | [docs](https://api.algodocs.com/#extractors) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://api.algodocs.com/#folders) |
| [Upload Document From Local Path](actions/upload-document-from-local-path.md) | `POST /document/upload_local/:extractorId/:folderId` | [docs](https://api.algodocs.com/#documents) |
| [Upload Document From URL](actions/upload-document-from-url.md) | `POST /document/upload_url/:extractorId/:folderId` | [docs](https://api.algodocs.com/#documents) |
| [Upload Document With Base64](actions/upload-document-with-base64.md) | `POST /document/upload_base64/:extractorId/:folderId` | [docs](https://api.algodocs.com/#documents) |
