# ONLYOFFICE DocSpace: Native API Reference

A consolidated summary of ONLYOFFICE DocSpace's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://api.onlyoffice.com/docspace/api-backend/usage-api/api/
- **API base URL:** `https://docspace-t0dtrp.onlyoffice.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.onlyoffice.com/docspace/api-backend/get-started/authentication/api-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `response`.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get File Settings](actions/get-file-settings.md) | `GET /api/2.0/files/settings` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-files-settings/) |
| [Get My Documents Section](actions/get-my-documents-section.md) | `GET /api/2.0/files/@my` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-my-folder/) |
| [Get My Profile](actions/get-my-profile.md) | `GET /api/2.0/people/@self` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-self-profile/) |
| [Get Portal Capabilities](actions/get-portal-capabilities.md) | `GET /api/2.0/capabilities` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-portal-capabilities/) |
| [Get Portal Information](actions/get-portal-information.md) | `GET /api/2.0/portal` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-portal-information/) |
| [Get Portal Settings](actions/get-portal-settings.md) | `GET /api/2.0/settings` | [docs](https://api.onlyoffice.com/docspace/api-backend/usage-api/get-settings/) |
