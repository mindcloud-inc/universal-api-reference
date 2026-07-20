# Base64.ai: Native API Reference

A consolidated summary of Base64.ai's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.base64.ai/
- **API base URL:** `https://base64.ai`

## Authentication

### API Key

Uses the Base64.ai login email plus API key in the Authorization header as ApiKey email:secret.

### Credentials

- **API Key:** `apiKey` · required
- **Login Email:** `loginEmail` · required · The Base64.ai account login email paired with the API key in Authorization: ApiKey email:secret.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://base64.ai/api/doc)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Result Question](actions/ask-result-question.md) | `POST /api/result/ask/:resultUuid` | [docs](https://apidoc.base64.ai/) |
| [Create Flow](actions/create-flow.md) | `POST /api/flow` | [docs](https://apidoc.base64.ai/) |
| [Delete Flow](actions/delete-flow.md) | `POST /api/flow/:flowId` | [docs](https://apidoc.base64.ai/) |
| [Get Asynchronous Scan Result](actions/get-asynchronous-scan-result.md) | `GET /api/scan/async/:asyncFileUUID` | [docs](https://apidoc.base64.ai/) |
| [Get Result](actions/get-result.md) | `GET /api/result/:resultUuid` | [docs](https://apidoc.base64.ai/) |
| [Get Result Review Status](actions/get-result-review-status.md) | `GET /api/result/:resultUuid` | [docs](https://apidoc.base64.ai/) |
| [Get User](actions/get-user.md) | `GET /api/auth/user` | [docs](https://apidoc.base64.ai/view/10132588/SWT5hfdz#39190748-5d86-4fba-a6ba-50d0df900e2f) |
| [List Flow Results](actions/list-flow-results.md) | `GET /api/result` | [docs](https://apidoc.base64.ai/) |
| [List Flows](actions/list-flows.md) | `GET /api/flow` | [docs](https://apidoc.base64.ai/) |
| [Mock Document Extraction](actions/mock-document-extraction.md) | `POST /mock/scan` | [docs](https://apidoc.base64.ai/) |
| [OCR Document by URL](actions/ocr-document-by-url.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Scan Document Asynchronously](actions/scan-document-asynchronously.md) | `POST /api/scan/async` | [docs](https://apidoc.base64.ai/) |
| [Scan Document by URL](actions/scan-document-by-url.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Scan Document into Flow](actions/scan-document-into-flow.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Scan Document Under Page Count](actions/scan-document-under-page-count.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Scan Document Until Page Number](actions/scan-document-until-page-number.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Scan Document with Document Types](actions/scan-document-with-document-types.md) | `POST /api/scan` | [docs](https://apidoc.base64.ai/) |
| [Update Flow](actions/update-flow.md) | `POST /api/flow/:flowId` | [docs](https://apidoc.base64.ai/) |
