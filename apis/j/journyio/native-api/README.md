# Journy.io: Native API Reference

A consolidated summary of Journy.io's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developers.journy.io/
- **OpenAPI specification:** https://api.journy.io/spec.json
- **API base URL:** `https://api.journy.io`

## Authentication

### API Key

Use a Journy.io API key from the Connections screen.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developers.journy.io/#section/Backend/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Users to Account](actions/add-users-to-account.md) | `POST /accounts/users/add` | [docs](https://developers.journy.io/#operation/addUserToAccount) |
| [Create or Update Account](actions/create-or-update-account.md) | `POST /accounts/upsert` | [docs](https://developers.journy.io/#operation/upsertAccount) |
| [Create or Update User](actions/create-or-update-user.md) | `POST /users/upsert` | [docs](https://developers.journy.io/#operation/upsertUser) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts` | [docs](https://developers.journy.io/#operation/deleteAccount) |
| [Delete User](actions/delete-user.md) | `DELETE /users` | [docs](https://developers.journy.io/#operation/deleteUser) |
| [Get Tracking Snippet](actions/get-tracking-snippet.md) | `GET /tracking/snippet` | [docs](https://developers.journy.io/#operation/getTrackingSnippet) |
| [Link Web Activity to User](actions/link-web-activity-to-user.md) | `POST /link` | [docs](https://developers.journy.io/#operation/link) |
| [List Account Properties](actions/list-account-properties.md) | `GET /properties/accounts` | [docs](https://developers.journy.io/#operation/getAccountProperties) |
| [List Account Segments](actions/list-account-segments.md) | `GET /segments/accounts` | [docs](https://developers.journy.io/#operation/getAccountSegments) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developers.journy.io/#operation/getEvents) |
| [List User Properties](actions/list-user-properties.md) | `GET /properties/users` | [docs](https://developers.journy.io/#operation/getUserProperties) |
| [List User Segments](actions/list-user-segments.md) | `GET /segments/users` | [docs](https://developers.journy.io/#operation/getUserSegments) |
| [Remove Users from Account](actions/remove-users-from-account.md) | `POST /accounts/users/remove` | [docs](https://developers.journy.io/#operation/removeUserFromAccount) |
| [Track Event](actions/track-event.md) | `POST /track` | [docs](https://developers.journy.io/#operation/trackEvent) |
| [Validate API Key](actions/validate-api-key.md) | `GET /validate` | [docs](https://developers.journy.io/#operation/getValidity) |
