# Deftform: Native API Reference

A consolidated summary of Deftform's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://help.deftform.com/api
- **API base URL:** `https://deftform.com/api/v1`

## Authentication

### Access Token

Authenticate Deftform API requests with a workspace access token sent as a Bearer token.

### Credentials

- **Access Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.deftform.com/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Form Response](actions/add-form-response.md) | `POST /forms/:formId/response` | [docs](https://help.deftform.com/api/endpoints) |
| [Get Submission PDF](actions/get-submission-pdf.md) | `GET /response/:uuid/pdf` | [docs](https://help.deftform.com/api/endpoints) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspace` | [docs](https://help.deftform.com/api/endpoints) |
| [List Form Fields](actions/list-form-fields.md) | `GET /forms/:formId/fields` | [docs](https://help.deftform.com/api/endpoints) |
| [List Form Responses](actions/list-form-responses.md) | `GET /responses/:formId` | [docs](https://help.deftform.com/api/endpoints) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://help.deftform.com/api/endpoints) |
| [Update Form Settings](actions/update-form-settings.md) | `POST /forms/:formId/settings` | [docs](https://help.deftform.com/api/endpoints) |
