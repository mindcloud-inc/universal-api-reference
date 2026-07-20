# Eledo: Native API Reference

A consolidated summary of Eledo's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://eledo.online/documentation/api_reference
- **API base URL:** `https://eledo.online/api/RESTv1`

## Authentication

### API Key

Connect to Eledo with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://eledo.online/documentation/api_reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create File](actions/create-file.md) | `POST /CreateFile` | [docs](https://eledo.online/documentation/api_reference/create_file) |
| [Download File](actions/download-file.md) | `GET /Download/:file_id` | [docs](https://eledo.online/documentation/api_reference/download) |
| [Generate PDF](actions/generate-pdf.md) | `POST /Generate` | [docs](https://eledo.online/documentation/api_reference/generate) |
| [Get Profile](actions/get-profile.md) | `GET /Profile` | [docs](https://eledo.online/documentation/api_reference/profile) |
| [Get Template Schema](actions/get-template-schema.md) | `GET /Schema/:template_id/:template_version` | [docs](https://eledo.online/documentation/api_reference/schema) |
| [List Templates](actions/list-templates.md) | `GET /List` | [docs](https://eledo.online/documentation/api_reference/list) |
