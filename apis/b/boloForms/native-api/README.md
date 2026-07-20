# BoloForms: Native API Reference

A consolidated summary of BoloForms's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://developer.boloforms.com/
- **API base URL:** `https://sapi.boloforms.com/signature`

## Authentication

### API Key

Connect with a BoloSign API key and workspace ID. BoloSign requests require the API key plus a workspace-scoped `workspaceId` header.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · BoloSign workspace ID required for document list requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bolosign-developer-docs.readme.io/reference/intro/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `pagination.totalPages`. The current page number is read from `pagination.currentPage`.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Form Responses](actions/get-form-responses.md) | `GET /get-form-responses` | [docs](https://bolosign-developer-docs.readme.io/reference/get_get-form-responses) |
| [Get Template Respondents](actions/get-template-respondents.md) | `GET /get-template-respondent` | [docs](https://bolosign-developer-docs.readme.io/reference/get_get-template-respondent-1) |
| [List Documents](actions/list-documents.md) | `GET /get-documents` | [docs](https://bolosign-developer-docs.readme.io/reference/get_get-documents-1) |
| [Send Template For Signing](actions/send-template-for-signing.md) | `POST /pdf-template-lambda` | [docs](https://bolosign-developer-docs.readme.io/reference/post_pdf-template-lambda-1) |
