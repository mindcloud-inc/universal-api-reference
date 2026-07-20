# Better Stack Uptime: Native API Reference

A consolidated summary of Better Stack Uptime's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://betterstack.com/docs/uptime/api/
- **API base URL:** `https://uptime.betterstack.com/api`

## Authentication

### API Key

Bearer token for the Better Stack Uptime API

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://betterstack.com/docs/uptime/api/getting-an-api-token/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_name` | query | `string` | no | Optional Better Stack team name when a global token is used across multiple teams |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `pagination.next`.

## Pagination

Use `per_page` in the query string to set the page size (default 50; maximum 250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Incident](actions/acknowledge-incident.md) | `POST /v3/incidents/:incidentId/acknowledge` | [docs](https://betterstack.com/docs/uptime/api/acknowledge-an-ongoing-incident/) |
| [Create Comment](actions/create-comment.md) | `POST /v2/incidents/:incidentId/comments` | [docs](https://betterstack.com/docs/uptime/api/create-a-new-comment/) |
| [Create Escalation Policy](actions/create-escalation-policy.md) | `POST /v3/policies` | [docs](https://betterstack.com/docs/uptime/api/create-escalation-policy/) |
| [Create Heartbeat](actions/create-heartbeat.md) | `POST /v2/heartbeats` | [docs](https://betterstack.com/docs/uptime/api/create-a-hearbeat/) |
| [Create Incident](actions/create-incident.md) | `POST /v3/incidents` | [docs](https://betterstack.com/docs/uptime/api/create-a-new-incident/) |
| [Create Monitor](actions/create-monitor.md) | `POST /v2/monitors` | [docs](https://betterstack.com/docs/uptime/api/create-a-new-monitor/) |
| [Create On-Call Calendar](actions/create-on-call-calendar.md) | `POST /v2/on-calls` | [docs](https://betterstack.com/docs/uptime/api/create-on-call-calendar/) |
| [Create Status Page](actions/create-status-page.md) | `POST /v2/status-pages` | [docs](https://betterstack.com/docs/uptime/api/create-a-new-status-page/) |
| [Delete Heartbeat](actions/delete-heartbeat.md) | `DELETE /v2/heartbeats/:heartbeat_id` | [docs](https://betterstack.com/docs/uptime/api/delete-existing-heartbeat/) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /v2/monitors/:monitor_id` | [docs](https://betterstack.com/docs/uptime/api/delete-an-existing-monitor/) |
| [Get Heartbeat](actions/get-heartbeat.md) | `GET /v2/heartbeats/:heartbeat_id` | [docs](https://betterstack.com/docs/uptime/api/get-a-single-hearbeat/) |
| [Get Heartbeat Availability Summary](actions/get-heartbeat-availability-summary.md) | `GET /v2/heartbeats/:heartbeat_id/availability` | [docs](https://betterstack.com/docs/uptime/api/get-a-heartbeats-availability-summary/) |
| [Get Incident](actions/get-incident.md) | `GET /v3/incidents/:incidentId` | [docs](https://betterstack.com/docs/uptime/api/list-a-single-incident/) |
| [Get Monitor](actions/get-monitor.md) | `GET /v2/monitors/:monitor_id` | [docs](https://betterstack.com/docs/uptime/api/get-a-single-monitor/) |
| [Get Monitor Availability Summary](actions/get-monitor-availability-summary.md) | `GET /v2/monitors/:monitor_id/sla` | [docs](https://betterstack.com/docs/uptime/api/get-a-monitors-availability-summary/) |
| [Get Monitor Response Times](actions/get-monitor-response-times.md) | `GET /v2/monitors/:monitor_id/response-times` | [docs](https://betterstack.com/docs/uptime/api/get-monitors-response-times/) |
| [Get On-Call Calendar](actions/get-on-call-calendar.md) | `GET /v2/on-calls/:scheduleId` | [docs](https://betterstack.com/docs/uptime/api/get-a-single-on-call-calendar/) |
| [Get Status Page](actions/get-status-page.md) | `GET /v2/status-pages/:statusPageId` | [docs](https://betterstack.com/docs/uptime/api/get-a-single-status-page/) |
| [List Comments](actions/list-comments.md) | `GET /v2/incidents/:incidentId/comments` | [docs](https://betterstack.com/docs/uptime/api/list-all-comments/) |
| [List Escalation Policies](actions/list-escalation-policies.md) | `GET /v3/policies` | [docs](https://betterstack.com/docs/uptime/api/list-all-escalation-policies/) |
| [List Heartbeats](actions/list-heartbeats.md) | `GET /v2/heartbeats` | [docs](https://betterstack.com/docs/uptime/api/list-all-existing-hearbeats/) |
| [List Incidents](actions/list-incidents.md) | `GET /v3/incidents` | [docs](https://betterstack.com/docs/uptime/api/list-all-incidents/) |
| [List Monitors](actions/list-monitors.md) | `GET /v2/monitors` | [docs](https://betterstack.com/docs/uptime/api/list-all-existing-monitors/) |
| [List On-Call Calendars](actions/list-on-call-calendars.md) | `GET /v2/on-calls` | [docs](https://betterstack.com/docs/uptime/api/list-all-existing-on-call-calendars/) |
| [List Status Pages](actions/list-status-pages.md) | `GET /v2/status-pages` | [docs](https://betterstack.com/docs/uptime/api/list-all-existing-status-pages/) |
| [Resolve Incident](actions/resolve-incident.md) | `POST /v3/incidents/:incidentId/resolve` | [docs](https://betterstack.com/docs/uptime/api/resolve-an-ongoing-incident/) |
| [Update Heartbeat](actions/update-heartbeat.md) | `PATCH /v2/heartbeats/:heartbeat_id` | [docs](https://betterstack.com/docs/uptime/api/update-existing-hearbeat/) |
| [Update Monitor](actions/update-monitor.md) | `PATCH /v2/monitors/:monitor_id` | [docs](https://betterstack.com/docs/uptime/api/update-an-existing-monitor/) |
