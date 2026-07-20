# LogRocket: Native API Reference

A consolidated summary of LogRocket's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.logrocket.com/docs/introduction
- **API base URL:** `https://api.logrocket.com/v1`

## Authentication

### API Key

Authenticate requests to LogRocket REST APIs using a project-scoped API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `orgId` · required · The first segment of your LogRocket App ID, shown as <org_id>/<project_id> in Project Settings.
- **Project ID:** `projectId` · required · The second segment of your LogRocket App ID, shown as <org_id>/<project_id> in Project Settings.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.logrocket.com/docs/session-highlights-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Highlights Result](actions/get-highlights-result.md) | `GET /orgs/:orgId/apps/:projectId/highlights/` | [docs](https://docs.logrocket.com/docs/session-highlights-api) |
| [Request User Highlights](actions/request-user-highlights.md) | `POST /orgs/:orgId/apps/:projectId/highlights/` | [docs](https://docs.logrocket.com/docs/session-highlights-api) |
| [Update User Information](actions/update-user-information.md) | `PUT /orgs/:orgId/apps/:projectId/users/:userId` | [docs](https://docs.logrocket.com/docs/user-identification-api) |
