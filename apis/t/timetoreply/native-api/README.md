# Timetoreply: Native API Reference

A consolidated summary of Timetoreply's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://portal.timetoreply.com/api-docs
- **OpenAPI specification:** https://portal.timetoreply.com/api-docs.openapi
- **API base URL:** `https://portal.timetoreply.com`

## Authentication

### Personal Access Token

Authenticate with a Timetoreply personal access token generated in TOOLS > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://portal.timetoreply.com/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 15; maximum 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Comparative Report](actions/get-comparative-report.md) | `GET /api/reports/comparative` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-comparative) |
| [Get Contacts Report](actions/get-contacts-report.md) | `GET /api/reports/contact` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-contact) |
| [Get Group Mailboxes Report](actions/get-group-mailboxes-report.md) | `GET /api/reports/group-mailboxes` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-group-mailboxes) |
| [Get Interactions Report](actions/get-interactions-report.md) | `GET /api/reports/interactions` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-interactions) |
| [Get Overview Report](actions/get-overview-report.md) | `GET /api/reports/overview` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-overview) |
| [Get Productivity Report](actions/get-productivity-report.md) | `GET /api/reports/productivity` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-productivity) |
| [Get Profile](actions/get-profile.md) | `GET /api/me` | [docs](https://portal.timetoreply.com/api-docs#tools-GETapi-me) |
| [Get SLA Report](actions/get-sla-report.md) | `GET /api/reports/sla` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-sla) |
| [Get Teams Report](actions/get-teams-report.md) | `GET /api/reports/teams` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-teams) |
| [Get Trend Report](actions/get-trend-report.md) | `GET /api/reports/trend` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-trend) |
| [List Agent Alerts](actions/list-agent-alerts.md) | `GET /api/reports/alerts/:agent_id` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-alerts--agent_id-) |
| [List Alerts](actions/list-alerts.md) | `GET /api/reports/alerts` | [docs](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-alerts) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /api/entities/contact-groups` | [docs](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-contact-groups) |
| [List Contacts](actions/list-contacts.md) | `GET /api/entities/contacts` | [docs](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-contacts) |
| [List Conversation Logs](actions/list-conversation-logs.md) | `GET /api/logs/conversations` | [docs](https://portal.timetoreply.com/api-docs#logs-GETapi-logs-conversations) |
| [List Group Mailboxes](actions/list-group-mailboxes.md) | `GET /api/entities/group-mailboxes` | [docs](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-group-mailboxes) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /api/entities/mailboxes` | [docs](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-mailboxes) |
| [List Message Logs](actions/list-message-logs.md) | `GET /api/logs/messages` | [docs](https://portal.timetoreply.com/api-docs#logs-GETapi-logs-messages) |
| [List Teams](actions/list-teams.md) | `GET /api/entities/teams` | [docs](https://portal.timetoreply.com/api-docs#entities-GETapi-entities-teams) |
| [List Users](actions/list-users.md) | `GET /api/entities/users` | [docs](https://portal.timetoreply.com/api-docs#tools-GETapi-entities-users) |
