# <img src="https://images.mindcloud.co/apps/icons/savvy-cal_1773841790020.png" alt="SavvyCal logo" width="28" height="28"> SavvyCal: Universal API

Schedule meetings, manage booking links, webhooks, and workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/savvyCal/latest
- **Category:** Productivity / Project Management
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://savvycal.com
- **Vendor API docs:** https://developers.savvycal.com/category/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | PUT |  |
| [Create Event](actions/create-event.md) | POST |  |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Personal Scheduling Link](actions/create-personal-scheduling-link.md) | POST |  |
| [Create Scope Scheduling Link](actions/create-scope-scheduling-link.md) | POST |  |
| [Delete Scheduling Link](actions/delete-scheduling-link.md) | DELETE |  |
| [Duplicate Scheduling Link](actions/duplicate-scheduling-link.md) | POST |  |
| [Get Scheduling Link](actions/get-scheduling-link.md) | GET |  |
| [List Available Time Slots](actions/list-available-time-slots.md) | GET |  |
| [List Scheduling Links](actions/list-scheduling-links.md) | GET |  |
| [Toggle Scheduling Link](actions/toggle-scheduling-link.md) | PUT |  |
| [Update Scheduling Link](actions/update-scheduling-link.md) | PUT |  |

### Timezone Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Zone](actions/get-time-zone.md) | GET |  |
| [List Time Zones](actions/list-time-zones.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Rules](actions/list-workflow-rules.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |

