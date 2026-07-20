# RapidAPI: Native API Reference

A consolidated summary of RapidAPI's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.rapidapi.com/docs/platform-api-overview
- **API base URL:** `{baseUrlRest}`

## Authentication

### Platform API Key

Use a RapidAPI key from a team with Enterprise Access to the REST Platform API.

### Credentials

- **API Key:** `apiKey` · required
- **REST Request URL:** `baseUrlRest` · required · Copy the REST Platform API request URL from the Enterprise Hub Platform API code snippet.
- **REST Host:** `rapidapiHostRest` · required · Copy the x-rapidapi-host value from the Enterprise Hub Platform API code snippet.

Send these headers with each API request:

```http
x-rapidapi-key: <apiKey>
x-rapidapi-host: <rapidapiHostRest>
```

[Official authentication documentation](https://docs.rapidapi.com/docs/using-the-platform-api-basics)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get App](actions/get-app.md) | `GET /apps/{projectId}` | [docs](https://docs.rapidapi.com/docs/example-obtaining-apps-and-keys-for-users-and-teams) |
| [List APIs](actions/list-apis.md) | `GET /apis` | [docs](https://docs.rapidapi.com/docs/example-using-the-rest-platform-api-listing-all-apis) |
| [List App Keys](actions/list-app-keys.md) | `GET /apps/{projectId}/keys` | [docs](https://docs.rapidapi.com/docs/example-obtaining-apps-and-keys-for-users-and-teams) |
| [List Apps](actions/list-apps.md) | `GET /apps` | [docs](https://docs.rapidapi.com/docs/example-obtaining-apps-and-keys-for-users-and-teams) |
| [List Entity Roles](actions/list-entity-roles.md) | `GET /admin/entities/{entityId}/roles` | [docs](https://docs.rapidapi.com/docs/platform-api-overview) |
| [List Organization Teams](actions/list-organization-teams.md) | `GET /organizations/{orgId}/teams` | [docs](https://docs.rapidapi.com/docs/platform-api-overview) |
| [List Organizations](actions/list-organizations.md) | `GET /admin/organizations` | [docs](https://docs.rapidapi.com/docs/managing-collections) |
| [List User Teams](actions/list-user-teams.md) | `GET /admin/users/{userId}/teams` | [docs](https://docs.rapidapi.com/docs/on-behalf-of) |
| [List Users](actions/list-users.md) | `GET /admin/users` | [docs](https://docs.rapidapi.com/docs/on-behalf-of) |
| [Update User](actions/update-user.md) | `PUT /users/{userId}` | [docs](https://docs.rapidapi.com/docs/on-behalf-of) |
