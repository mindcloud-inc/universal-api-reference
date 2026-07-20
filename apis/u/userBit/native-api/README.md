# UserBit: Native API Reference

A consolidated summary of UserBit's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://userbit.com/content/api
- **API base URL:** `https://userbit.com/api`

## Authentication

### Firebase ID Token

Use a UserBit Firebase ID token for bearer-authenticated API calls.

### Credentials

- **ID Token:** `idToken` · required · Firebase ID token used as the UserBit bearer token.
- **Refresh Token:** `refreshToken` · required · Firebase refresh token used to mint a new ID token when UserBit returns Token Expired.
- **Firebase API Key:** `apiKey` · required · UserBit Firebase Web API key used with the Secure Token refresh endpoint.
- **Workspace ID:** `workspaceId` · required · Default UserBit workspace ID for workspace-scoped actions.
- **User ID:** `userId` · optional · Optional default UserBit user ID for tenant-scoped actions and note identifiers.

Send these headers with each API request:

```http
Authorization: Bearer <idToken>
```

[Official authentication documentation](https://userbit.com/content/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Note](actions/create-or-update-note.md) | `POST /v1/notes/create-update` | [docs](https://userbit.com/content/api#create-or-update-a-note) |
| [Create Survey Response](actions/create-survey-response.md) | `POST /v1/surveys/questions/list` | [docs](https://userbit.com/content/api#create-a-survey-response) |
| [List Insights](actions/list-insights.md) | `GET /v1/insights/list` | [docs](https://userbit.com/content/api#list-insights) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects/list` | [docs](https://userbit.com/content/api) |
| [List Survey Questions](actions/list-survey-questions.md) | `GET /v1/surveys/questions/list` | [docs](https://userbit.com/content/api#list-survey-questions) |
| [List Surveys](actions/list-surveys.md) | `GET /v1/surveys/list` | [docs](https://userbit.com/content/api#list-surveys) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces/list` | [docs](https://userbit.com/content/api#list-workspacesh3) |
