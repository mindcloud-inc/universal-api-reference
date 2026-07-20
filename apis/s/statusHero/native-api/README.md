# Status Hero: Native API Reference

A consolidated summary of Status Hero's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://api.statushero.com
- **API base URL:** `https://service.statushero.com/api/v1`

## Authentication

### API key

Header-based authentication using X-Team-ID and X-API-Key.

### Credentials

- **API Key:** `apiKey` · required
- **Team ID:** `teamId` · required · Status Hero team ID from Team Settings > API.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
X-Team-ID: <teamId>
```

[Official authentication documentation](https://api.statushero.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add member absence](actions/add-member-absence.md) | `POST /member_absences/:id` | [docs](https://api.statushero.com/#add-member-absence) |
| [Add status activity](actions/add-status-activity.md) | `POST /status_activities` | [docs](https://api.statushero.com/#add-a-status-activity) |
| [Add team absence](actions/add-team-absence.md) | `POST /team_absences` | [docs](https://api.statushero.com/#add-team-absence) |
| [Get comment](actions/get-comment.md) | `GET /comments/:id` | [docs](https://api.statushero.com/#comments) |
| [Get member](actions/get-member.md) | `GET /members/:id` | [docs](https://api.statushero.com/#get-a-specific-team-member) |
| [Get reaction](actions/get-reaction.md) | `GET /reactions/:id` | [docs](https://api.statushero.com/#reactions) |
| [Get report](actions/get-report.md) | `GET /reports/:id` | [docs](https://api.statushero.com/#get-a-specific-report) |
| [Get status](actions/get-status.md) | `GET /statuses/:id` | [docs](https://api.statushero.com/#get-a-specific-status) |
| [Get status activity](actions/get-status-activity.md) | `GET /status_activities/:id` | [docs](https://api.statushero.com/#get-a-specific-status-activity) |
| [List members](actions/list-members.md) | `GET /members` | [docs](https://api.statushero.com/#members) |
| [List reports](actions/list-reports.md) | `GET /reports` | [docs](https://api.statushero.com/#reports) |
| [List statuses](actions/list-statuses.md) | `GET /statuses` | [docs](https://api.statushero.com/#statuses) |
| [List statuses by tag](actions/list-statuses-by-tag.md) | `GET /tags/:tag` | [docs](https://api.statushero.com/#get-statuses-from-a-tag) |
| [List tags](actions/list-tags.md) | `GET /tags` | [docs](https://api.statushero.com/#tags) |
| [Remove member absence](actions/remove-member-absence.md) | `DELETE /member_absences/:id/:date` | [docs](https://api.statushero.com/#remove-member-absence) |
| [Remove team absence](actions/remove-team-absence.md) | `DELETE /team_absences/:date` | [docs](https://api.statushero.com/#remove-team-absence) |
