# <img src="https://images.mindcloud.co/apps/icons/unnamed-1_1774029215781.png" alt="Morgen logo" width="28" height="28"> Morgen: Universal API

Create and manage Morgen calendar events and tasks through the public API-key surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/morgen/latest
- **Category:** Productivity / Scheduling
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.morgen.so/
- **Vendor API docs:** https://docs.morgen.so/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Integration Accounts](actions/list-integration-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-integration-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from Morgen. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates an event in Morgen. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an event from Morgen. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Morgen. |
| [Update Event](actions/update-event.md) | PUT | Updates an event in Morgen. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves available integrations from Morgen. |

### Integration Account

| Action | Method | Description |
| --- | --- | --- |
| [List Integration Accounts](actions/list-integration-accounts.md) | GET | Retrieves connected integration accounts from Morgen. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Close Task](actions/close-task.md) | PUT | Marks a task as completed in Morgen. |
| [Create Task](actions/create-task.md) | POST | Creates a task in Morgen. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from Morgen. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Morgen. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Morgen. |
| [Reopen Task](actions/reopen-task.md) | PUT | Reopens a completed task in Morgen. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Morgen. |

