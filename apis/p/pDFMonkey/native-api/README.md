# PDFMonkey: Native API Reference

A consolidated summary of PDFMonkey's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://pdfmonkey.io/docs/api/
- **OpenAPI specification:** https://1206964087-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FknPix3PnJ9iEQrP2Sbuh%2Fuploads%2FjPkQvJBX0ucZwZ8p6fxS%2Fswagger.json?alt=media&token=280a1a4c-69b6-4de5-9abb-c53be7c6b549
- **API base URL:** `https://api.pdfmonkey.io/api/v1`

## Authentication

### API Key

Authenticate with your PDFMonkey API Secret Key using the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pdfmonkey.io/guides/first-api-call)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://pdfmonkey.io/docs/api/documents/#create-a-document) |
| [Create Template](actions/create-template.md) | `POST /document_templates` | [docs](https://pdfmonkey.io/docs/api/templates/#create-a-template) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://pdfmonkey.io/docs/api/documents/#delete-a-document) |
| [Delete Template](actions/delete-template.md) | `DELETE /document_templates/:id` | [docs](https://pdfmonkey.io/docs/api/templates/#delete-a-template) |
| [Generate Document Synchronously](actions/generate-document-synchronously.md) | `POST /documents/sync` | [docs](https://pdfmonkey.io/docs/api/documents/#synchronous-generation) |
| [Get Current User](actions/get-current-user.md) | `GET /current_user` | [docs](https://pdfmonkey.io/docs/api/authentication/#make-a-test-api-call) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://pdfmonkey.io/docs/api/documents/#get-a-document) |
| [Get Document Card](actions/get-document-card.md) | `GET /document_cards/:id` | [docs](https://pdfmonkey.io/docs/api/documents/#get-a-document) |
| [Get Template](actions/get-template.md) | `GET /document_templates/:id` | [docs](https://pdfmonkey.io/docs/api/templates/#get-a-template) |
| [List Documents](actions/list-documents.md) | `GET /document_cards` | [docs](https://pdfmonkey.io/docs/api/documents/#list-documents) |
| [List PDF Engines](actions/list-pdf-engines.md) | `GET /pdf_engines` | [docs](https://pdfmonkey.io/docs/api/templates/#pdf-engines) |
| [List Templates](actions/list-templates.md) | `GET /document_template_cards` | [docs](https://pdfmonkey.io/docs/api/templates/#list-templates) |
| [Update Document](actions/update-document.md) | `PUT /documents/:id` | [docs](https://pdfmonkey.io/docs/api/documents/#update-a-document) |
| [Update Template](actions/update-template.md) | `PUT /document_templates/:id` | [docs](https://pdfmonkey.io/docs/api/templates/#update-a-template) |
