# FormRobin: Native API Reference

A consolidated summary of FormRobin's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://formrobin.com/developer/docs/
- **API base URL:** `https://formrobin.com/api/v1`

## Authentication

### Personal Access Token

Authenticate with a FormRobin personal access token from Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://appsumooriginals.helpscoutdocs.com/article/835-formrobin-api-getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms/post) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms/{{id}}` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms~1{id}/delete) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://formrobin.com/developer/docs/#tag/User/paths/~1me/get) |
| [Get Form](actions/get-form.md) | `GET /forms/{{id}}` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms~1{id}/get) |
| [List Form Sessions](actions/list-form-sessions.md) | `GET /forms/{{id}}/sessions` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms~1{id}~1sessions/get) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms/get) |
| [Update Form](actions/update-form.md) | `PUT /forms/{{id}}` | [docs](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms~1{id}/put) |
