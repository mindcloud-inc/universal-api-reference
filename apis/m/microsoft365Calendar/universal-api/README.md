# <img src="https://images.mindcloud.co/apps/icons/microsoft-icon_1776116380940.png" alt="Microsoft 365 Calendar logo" width="28" height="28"> Microsoft 365 Calendar: Universal API

Access Microsoft 365 calendar data through Microsoft Graph, including calendars, events, and calendar views for the signed-in user.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365Calendar/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://outlook.office.com/calendar/
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/calendar?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from Microsoft 365 Calendar. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Accept Event](actions/accept-event.md) | PUT | Accepts an event invitation in Microsoft 365 Calendar. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Microsoft 365 Calendar. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Microsoft 365 Calendar. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Microsoft 365 Calendar. |
| [List Calendar View](actions/list-calendar-view.md) | GET | Retrieves events from Microsoft 365 Calendar for a time range. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Microsoft 365 Calendar. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Microsoft 365 Calendar. |

