# <img src="https://images.mindcloud.co/apps/icons/cronfree-time-scheduler_1774904232074.png" alt="Cronfree Time Scheduler logo" width="28" height="28"> Cronfree Time Scheduler: Universal API

Schedule and unschedule recurring webhook triggers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cronfreeTimeScheduler/latest
- **Category:** Productivity / Scheduling
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cronfree.com/
- **Vendor API docs:** https://docs.cronfree.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Schedule](actions/create-schedule.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "wdays[]": [
    "string"
  ],
  "months[]": [
    "string"
  ],
  "mdays[]": [
    "string"
  ],
  "hours[]": [
    "string"
  ],
  "minutes[]": [
    "string"
  ],
  "timezone": "string"
}'
```

## Actions (2)

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a new schedule in Cronfree Time Scheduler. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from Cronfree Time Scheduler. |

