# CallPage: Native API Reference

A consolidated summary of CallPage's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://callpage.github.io/documentation-rest/
- **API base URL:** `https://core.callpage.io/api/v1/external`

## Authentication

### API Key

Use the owner account's CallPage API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://knowledge.callpage.io/en/articles/3158869-how-to-set-up-callpage-integration-with-zapier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Users To Widget](actions/add-users-to-widget.md) | `POST /widgets/add-users` | [docs](https://callpage.github.io/documentation-rest/#add-users) |
| [Call Or Schedule](actions/call-or-schedule.md) | `POST /widgets/call-or-schedule` | [docs](https://callpage.github.io/documentation-rest/#call-or-schedule) |
| [Create Manager](actions/create-manager.md) | `POST /managers/create` | [docs](https://callpage.github.io/documentation-rest/#create-manager) |
| [Create SMS Message](actions/create-sms-message.md) | `POST /sms/create` | [docs](https://callpage.github.io/documentation-rest/#create-sms) |
| [Create User](actions/create-user.md) | `POST /users/create` | [docs](https://callpage.github.io/documentation-rest/#create-user) |
| [Create Voice Message](actions/create-voice-message.md) | `POST /voice/create` | [docs](https://callpage.github.io/documentation-rest/#create-voice-message) |
| [Create Widget](actions/create-widget.md) | `POST /widgets/create` | [docs](https://callpage.github.io/documentation-rest/#create-widget) |
| [Delete Manager](actions/delete-manager.md) | `POST /managers/delete` | [docs](https://callpage.github.io/documentation-rest/#delete-manager) |
| [Delete User](actions/delete-user.md) | `POST /users/delete` | [docs](https://callpage.github.io/documentation-rest/#delete-user) |
| [Delete Widget](actions/delete-widget.md) | `POST /widgets/delete` | [docs](https://callpage.github.io/documentation-rest/#delete-widget) |
| [Get Call](actions/get-call.md) | `GET https://core.callpage.io/api/v3/external/calls/{call_id}` | [docs](https://callpage.github.io/documentation-rest/#get-single-call) |
| [Get Manager](actions/get-manager.md) | `GET /managers/get` | [docs](https://callpage.github.io/documentation-rest/#get-manager) |
| [Get User](actions/get-user.md) | `GET /users/get` | [docs](https://callpage.github.io/documentation-rest/#get-user) |
| [Get Widget](actions/get-widget.md) | `GET /widgets/get` | [docs](https://callpage.github.io/documentation-rest/#get-widget) |
| [List Calls](actions/list-calls.md) | `GET https://core.callpage.io/api/v3/external/calls/history` | [docs](https://callpage.github.io/documentation-rest/#get-history) |
| [List Managers](actions/list-managers.md) | `GET /managers/all` | [docs](https://callpage.github.io/documentation-rest/#get-all-managers) |
| [List SMS Messages](actions/list-sms-messages.md) | `GET /sms/all` | [docs](https://callpage.github.io/documentation-rest/#get-all-smss) |
| [List Users](actions/list-users.md) | `GET /users/all` | [docs](https://callpage.github.io/documentation-rest/#get-all-users) |
| [List Voice Messages](actions/list-voice-messages.md) | `GET /voice/all` | [docs](https://callpage.github.io/documentation-rest/#get-all-voice-messages) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets/all` | [docs](https://callpage.github.io/documentation-rest/#get-all-widgets) |
| [Reset SMS Messages](actions/reset-sms-messages.md) | `POST /sms/reset` | [docs](https://callpage.github.io/documentation-rest/#reset-sms) |
| [Reset Voice Messages](actions/reset-voice-messages.md) | `POST /voice/reset` | [docs](https://callpage.github.io/documentation-rest/#reset-voice-message) |
| [Start Widget Call](actions/start-widget-call.md) | `POST /widgets/call` | [docs](https://callpage.github.io/documentation-rest/#simple-call) |
| [Update Call Field](actions/update-call-field.md) | `PATCH /calls/{call}/fields/{field}` | [docs](https://callpage.github.io/documentation-rest/#update-field) |
| [Update Manager](actions/update-manager.md) | `POST /managers/update` | [docs](https://callpage.github.io/documentation-rest/#update-manager) |
| [Update SMS Message](actions/update-sms-message.md) | `POST /sms/update` | [docs](https://callpage.github.io/documentation-rest/#update-sms) |
| [Update User](actions/update-user.md) | `POST /users/update` | [docs](https://callpage.github.io/documentation-rest/#update-user) |
| [Update Voice Message](actions/update-voice-message.md) | `POST /voice/update` | [docs](https://callpage.github.io/documentation-rest/#update-voice-message) |
| [Update Widget](actions/update-widget.md) | `POST /widgets/update` | [docs](https://callpage.github.io/documentation-rest/#update-widget) |
