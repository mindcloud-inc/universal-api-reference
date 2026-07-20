# WebAutomation.io: Native API Reference

A consolidated summary of WebAutomation.io's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://webautomation.io/api/redoc/
- **API base URL:** `https://webautomation.io/api`

## Authentication

### Basic Auth

Use your WebAutomation.io account email and password to authorize API requests.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://webautomation.io/support/webautomation-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Extractor](actions/activate-extractor.md) | `POST /activate_extractor/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [Add Starter Links](actions/add-starter-links.md) | `POST /extractors/start_urls/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [Delete Starter Links](actions/delete-starter-links.md) | `DELETE /extractors/start_urls/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [Get Session](actions/get-session.md) | `GET /sessions/{{SESSIONID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [Get Session Data](actions/get-session-data.md) | `GET /sessions/data/{{SESSIONID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [List Extractor Domains](actions/list-extractor-domains.md) | `GET /add_extractor_domain/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [List Extractor Variables](actions/list-extractor-variables.md) | `GET /extractor_variables/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [List Extractors](actions/list-extractors.md) | `GET /extractors/` | [docs](https://webautomation.io/api/redoc/) |
| [List Extractors by Domain](actions/list-extractors-by-domain.md) | `GET /extractors/{{domain}}/` | [docs](https://webautomation.io/api/redoc/) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions/` | [docs](https://webautomation.io/api/redoc/) |
| [List Starter Links](actions/list-starter-links.md) | `GET /extractors/start_urls/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
| [Update Extractor Variables](actions/update-extractor-variables.md) | `PUT /extractor_variables/{{EXTRACTOR_ID}}/` | [docs](https://webautomation.io/api/redoc/) |
