# Storerocket: Native API Reference

A consolidated summary of Storerocket's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://storerocket.io
- **API base URL:** `https://storerocket.io/api/v2`

## Authentication

### API Key

Use a StoreRocket API token from the StoreRocket account settings. Runtime requests use Authorization: Bearer <API token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://storerocket.io)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | `POST /projects/:projectId/locations` | [docs](https://storerocket.io/api/v2/projects/:projectId/locations) |
| [Delete Location](actions/delete-location.md) | `DELETE /projects/:projectId/locations/:locationId` | [docs](https://storerocket.io/api/v2/projects/:projectId/locations/:locationId) |
| [Get Location](actions/get-location.md) | `GET /projects/:projectId/locations/:locationId` | [docs](https://storerocket.io/api/v2/projects/:projectId/locations/:locationId) |
| [Get User Info](actions/get-user-info.md) | `GET /user` | [docs](https://storerocket.io/api/v2/user) |
| [List Locations](actions/list-locations.md) | `GET /projects/:projectId/locations` | [docs](https://storerocket.io/api/v2/projects/:projectId/locations) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://storerocket.io/api/v2/projects) |
| [Update Location](actions/update-location.md) | `PUT /projects/:projectId/locations/:locationId` | [docs](https://storerocket.io/api/v2/projects/:projectId/locations/:locationId) |
