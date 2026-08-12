# PostHog: Native API Reference

A consolidated summary of PostHog's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://posthog.com/docs/api
- **API base URL:** `https://us.posthog.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://posthog.com/docs/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/plain, */*` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add or Invite Members](actions/add-or-invite-members.md) | `POST /organizations/:organizationId/invites/` | [docs](https://posthog.com/docs/api/invites) |
| [Get Session Recording](actions/get-session-recording.md) | `GET /projects/:project_id/session_recordings/:id/` | [docs](https://posthog.com/docs/api/session-recordings) |
| [List Activity Log](actions/list-activity-log.md) | `GET /projects/:projectId/activity_log/` | [docs](https://posthog.com/docs/api/activity-log) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://posthog.com/docs/api/organizations) |
| [List Persons](actions/list-persons.md) | `GET /environments/:projectId/persons` | [docs](https://posthog.com/docs/api/persons) |
| [List Projects](actions/list-projects.md) | `GET /organizations/:organizationId/projects` | [docs](https://posthog.com/docs/api/projects) |
| [List Session Recordings](actions/list-session-recordings.md) | `GET /projects/:project_id/session_recordings/` | [docs](https://posthog.com/docs/api/session-recordings) |
| [Query](actions/query.md) | `POST /projects/:projectId/query/` | [docs](https://posthog.com/docs/api/query) |
