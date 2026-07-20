# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-zoom-us-48x48_1776886429252.png" alt="Zoom Scheduler logo" width="28" height="28"> Zoom Scheduler: Universal API

Create schedules, manage availability, share booking links, and work with scheduled events in Zoom Scheduler.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zoomScheduler/latest
- **Category:** Productivity / Scheduling
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zoom.com/en/products/appointment-scheduler/
- **Vendor API docs:** https://developers.zoom.us/docs/api/scheduler/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomScheduler/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams for a user from Zoom Scheduler. |

