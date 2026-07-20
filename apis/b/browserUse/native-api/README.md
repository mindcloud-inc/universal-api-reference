# Browser Use: Native API Reference

A consolidated summary of Browser Use's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.browser-use.com/cloud/api-reference
- **OpenAPI specification:** https://docs.browser-use.com/cloud/openapi/v3.json
- **API base URL:** `https://api.browser-use.com/api/v3`

## Authentication

### API Key

Authenticate to Browser Use Cloud with an API key sent in the X-Browser-Use-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.browser-use.com/cloud/api-reference)

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

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Browser Session](actions/create-browser-session.md) | `POST /browsers` | [docs](https://docs.browser-use.com/cloud/api-v3/browsers/create-browser-session) |
| [Create Profile](actions/create-profile.md) | `POST /profiles` | [docs](https://docs.browser-use.com/cloud/api-v3/profiles/create-profile) |
| [Create Session](actions/create-session.md) | `POST /sessions` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/create-session) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/create-workspace) |
| [Create Workspace File Upload URLs](actions/create-workspace-file-upload-urls.md) | `POST /workspaces/:workspace_id/files/upload` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/upload-workspace-files) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /profiles/:profile_id` | [docs](https://docs.browser-use.com/cloud/api-v3/profiles/delete-browser-profile) |
| [Delete Session](actions/delete-session.md) | `DELETE /sessions/:session_id` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/delete-session) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/:workspace_id` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/delete-workspace) |
| [Delete Workspace File](actions/delete-workspace-file.md) | `DELETE /workspaces/:workspace_id/files` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/delete-workspace-file) |
| [Get Account Billing](actions/get-account-billing.md) | `GET /billing/account` | [docs](https://docs.browser-use.com/cloud/api-reference) |
| [Get Browser Session](actions/get-browser-session.md) | `GET /browsers/:session_id` | [docs](https://docs.browser-use.com/cloud/api-v3/browsers/get-browser-session) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/:profile_id` | [docs](https://docs.browser-use.com/cloud/api-v3/profiles/get-profile) |
| [Get Session](actions/get-session.md) | `GET /sessions/:session_id` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/get-session) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspace_id` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/get-workspace) |
| [Get Workspace Size](actions/get-workspace-size.md) | `GET /workspaces/:workspace_id/size` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/get-workspace-size) |
| [List Browser Sessions](actions/list-browser-sessions.md) | `GET /browsers` | [docs](https://docs.browser-use.com/cloud/api-v3/browsers/list-browser-sessions) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://docs.browser-use.com/cloud/api-v3/profiles/list-profiles) |
| [List Session Messages](actions/list-session-messages.md) | `GET /sessions/:session_id/messages` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/list-session-messages) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/list-sessions) |
| [List Workspace Files](actions/list-workspace-files.md) | `GET /workspaces/:workspace_id/files` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/list-workspace-files) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/list-workspaces) |
| [Stop Browser Session](actions/stop-browser-session.md) | `PATCH /browsers/:session_id` | [docs](https://docs.browser-use.com/cloud/api-v3/browsers/update-browser-session) |
| [Stop Session](actions/stop-session.md) | `POST /sessions/:session_id/stop` | [docs](https://docs.browser-use.com/cloud/api-v3/sessions/stop-session) |
| [Update Profile](actions/update-profile.md) | `PATCH /profiles/:profile_id` | [docs](https://docs.browser-use.com/cloud/api-v3/profiles/update-profile) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /workspaces/:workspace_id` | [docs](https://docs.browser-use.com/cloud/api-v3/workspaces/update-workspace) |
