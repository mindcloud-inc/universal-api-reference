# DocuPotion: Native API Reference

A consolidated summary of DocuPotion's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docupotion.com/api-docs
- **API base URL:** `https://api.docupotion.com`

## Authentication

### API Key

Authenticate with your DocuPotion API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docupotion.com/api-docs#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Create Document to Connected S3](actions/create-document-to-connected-s3.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Create PDF Base64](actions/create-pdf-base64.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Create PDF URL](actions/create-pdf-url.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Create PNG Base64](actions/create-png-base64.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Create PNG URL](actions/create-png-url.md) | `POST /v1/create` | [docs](https://docupotion.com/api-docs#create-document) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://docupotion.com/api-docs#account) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://docupotion.com/api-docs#list-templates) |
