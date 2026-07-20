# AnyDB: Native API Reference

A consolidated summary of AnyDB's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.anydb.com/support/integrations/api/
- **OpenAPI specification:** https://www.anydb.com/openapi/spec.yaml
- **API base URL:** `https://app.anydb.com`

## Authentication

### API Key

Authenticate with an AnyDB API key plus the email address associated with that key.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required · The email address for the AnyDB account that owns the API key.

Send these headers with each API request:

```http
x-anydb-email: <email>
x-anydb-api-key: <apiKey>
```

[Official authentication documentation](https://www.anydb.com/support/integrations/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Upload](actions/complete-upload.md) | `PUT /api/integrations/ext/completeupload` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Create Record](actions/create-record.md) | `POST /api/integrations/ext/createrecord` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Duplicate Record](actions/duplicate-record.md) | `POST /api/integrations/ext/copyrecord` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Get Download URL](actions/get-download-url.md) | `GET /api/integrations/ext/download` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Get Record](actions/get-record.md) | `GET /api/integrations/ext/record` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Get Upload URL](actions/get-upload-url.md) | `GET /api/integrations/ext/getuploadurl` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [List Databases For Team](actions/list-databases-for-team.md) | `GET /api/integrations/ext/listdbsforteam` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [List Records](actions/list-records.md) | `GET /api/integrations/ext/list` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [List Teams](actions/list-teams.md) | `GET /api/integrations/ext/listteams` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Remove Record From Parents](actions/remove-record-from-parents.md) | `DELETE /api/integrations/ext/remove` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Search Records](actions/search-records.md) | `GET /api/integrations/ext/search` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Update Record](actions/update-record.md) | `PUT /api/integrations/ext/updaterecord` | [docs](https://www.anydb.com/openapi/spec.yaml) |
| [Validate API Key And Email](actions/validate-api-key-and-email.md) | `POST /api/integrations/ext/checkauth` | [docs](https://www.anydb.com/openapi/spec.yaml) |
