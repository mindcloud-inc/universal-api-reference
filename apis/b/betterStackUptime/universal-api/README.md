# <img src="https://images.mindcloud.co/apps/icons/bs-2-2_1777486037973.png" alt="Better Stack Uptime logo" width="28" height="28"> Better Stack Uptime: Universal API

Monitor services, manage incidents, and share status pages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/betterStackUptime/latest
- **Category:** IT Operations / Observability
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://betterstack.com/uptime
- **Vendor API docs:** https://betterstack.com/docs/uptime/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Heartbeat](actions/get-heartbeat.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-heartbeat?connectionId=$CONNECTION_ID&heartbeatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment on an incident in Better Stack Uptime. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments for an incident in Better Stack Uptime. |

### Escalation Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Escalation Policy](actions/create-escalation-policy.md) | POST | Creates a new escalation policy in Better Stack Uptime. |
| [List Escalation Policies](actions/list-escalation-policies.md) | GET | Retrieves escalation policies from Better Stack Uptime. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Incident](actions/acknowledge-incident.md) | PUT | Acknowledges an ongoing incident in Better Stack Uptime. |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in Better Stack Uptime. |
| [Get Incident](actions/get-incident.md) | GET | Retrieves an incident from Better Stack Uptime. |
| [List Incidents](actions/list-incidents.md) | GET | Retrieves incidents from Better Stack Uptime. |
| [Resolve Incident](actions/resolve-incident.md) | PUT | Resolves an ongoing incident in Better Stack Uptime. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves monitors from Better Stack Uptime. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a new monitor in Better Stack Uptime. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes an existing monitor from Better Stack Uptime. |
| [Get Monitor](actions/get-monitor.md) | GET | Retrieves a monitor from Better Stack Uptime. |
| [Get Monitor Availability Summary](actions/get-monitor-availability-summary.md) | GET | Retrieves an availability summary for a monitor in Better Stack Uptime. |
| [Get Monitor Response Times](actions/get-monitor-response-times.md) | GET | Retrieves response times for a monitor in Better Stack Uptime. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in Better Stack Uptime. |

### On-call Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create On-Call Calendar](actions/create-on-call-calendar.md) | POST | Creates a new on-call schedule in Better Stack Uptime. |
| [Get On-Call Calendar](actions/get-on-call-calendar.md) | GET | Retrieves an on-call schedule from Better Stack Uptime. |
| [List On-Call Calendars](actions/list-on-call-calendars.md) | GET | Retrieves on-call schedules from Better Stack Uptime. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Heartbeat](actions/create-heartbeat.md) | POST | Creates a new heartbeat in Better Stack Uptime. |
| [Delete Heartbeat](actions/delete-heartbeat.md) | DELETE | Deletes an existing heartbeat from Better Stack Uptime. |
| [Get Heartbeat](actions/get-heartbeat.md) | GET | Retrieves a heartbeat from Better Stack Uptime. |
| [Get Heartbeat Availability Summary](actions/get-heartbeat-availability-summary.md) | GET | Retrieves an availability summary for a heartbeat in Better Stack Uptime. |
| [List Heartbeats](actions/list-heartbeats.md) | GET | Retrieves heartbeats from Better Stack Uptime. |
| [Update Heartbeat](actions/update-heartbeat.md) | PUT | Updates an existing heartbeat in Better Stack Uptime. |

### Status Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Status Page](actions/create-status-page.md) | POST | Creates a new status page in Better Stack Uptime. |
| [Get Status Page](actions/get-status-page.md) | GET | Retrieves a status page from Better Stack Uptime. |
| [List Status Pages](actions/list-status-pages.md) | GET | Retrieves status pages from Better Stack Uptime. |

