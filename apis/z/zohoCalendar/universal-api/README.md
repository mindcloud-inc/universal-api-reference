# <img src="https://images.mindcloud.co/apps/icons/a7222963c3a5d48ad819450ccceb565b_1775165626147.png" alt="Zoho Calendar logo" width="28" height="28"> Zoho Calendar: Universal API

Manage calendars, schedule events, and coordinate team availability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoCalendar/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/calendar/
- **Vendor API docs:** https://www.zoho.com/calendar/help/api/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new personal calendar in Zoho Calendar. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from Zoho Calendar. |
| [Get Calendar Details](actions/get-calendar-details.md) | GET | Retrieves details for a calendar in Zoho Calendar. |
| [Get Shared Calendar Details](actions/get-shared-calendar-details.md) | GET | Retrieves details for a shared calendar in Zoho Calendar. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves user calendars from Zoho Calendar. |
| [Share Calendar](actions/share-calendar.md) | PUT | Updates calendar sharing in Zoho Calendar. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in Zoho Calendar. |

### Calendar Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Settings](actions/get-calendar-settings.md) | GET | Retrieves calendar settings from Zoho Calendar. |
| [Update Calendar Settings](actions/update-calendar-settings.md) | PUT | Updates calendar settings in Zoho Calendar. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Zoho Calendar. |
| [Create Event Using Smart Add](actions/create-event-using-smart-add.md) | POST | Creates a new event in Zoho Calendar using Smart Add. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Zoho Calendar. |
| [Get Event By Instance](actions/get-event-by-instance.md) | GET | Retrieves instances of a recurring event in Zoho Calendar. |
| [Get Event Details](actions/get-event-details.md) | GET | Retrieves details for an event in Zoho Calendar. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Zoho Calendar calendar. |
| [Move Event](actions/move-event.md) | PUT | Moves an event to another calendar in Zoho Calendar. |
| [Partial Update Event](actions/partial-update-event.md) | PUT | Updates specific event fields in Zoho Calendar. |
| [Search Events](actions/search-events.md) | GET | Finds events in a Zoho Calendar calendar. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Zoho Calendar. |

### Free Busy

| Action | Method | Description |
| --- | --- | --- |
| [Get User Free Busy Details](actions/get-user-free-busy-details.md) | GET | Retrieves user free/busy details from Zoho Calendar. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Attendees Details](actions/get-group-attendees-details.md) | GET | Retrieves group attendee details for an event in Zoho Calendar. |
| [List Group Calendars](actions/list-group-calendars.md) | GET | Retrieves group calendars from Zoho Calendar. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Details](actions/get-notification-details.md) | GET | Retrieves notification details from Zoho Calendar. |
| [Update Notification Details](actions/update-notification-details.md) | PUT | Updates notification details in Zoho Calendar. |

