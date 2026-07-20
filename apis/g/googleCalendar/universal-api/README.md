# <img src="https://images.mindcloud.co/apps/icons/cal_1744049422991.png" alt="Google Calendar logo" width="28" height="28"> Google Calendar: Universal API

Schedule events, share calendars, book time, and coordinate meetings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleCalendar/latest
- **Category:** Productivity / Scheduling
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calendar.google.com/
- **Vendor API docs:** https://developers.google.com/workspace/calendar/api/v3/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Acl Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create ACL Rule](actions/create-acl-rule.md) | POST | Creates a new calendar ACL rule in Google Calendar. |
| [Delete ACL Rule](actions/delete-acl-rule.md) | DELETE | Deletes an existing calendar ACL rule from Google Calendar. |
| [Get ACL Rule](actions/get-acl-rule.md) | GET | Retrieves a calendar ACL rule from Google Calendar. |
| [List ACL Rules](actions/list-acl-rules.md) | GET | Retrieves calendar ACL rules from Google Calendar. |
| [Update ACL Rule](actions/update-acl-rule.md) | PUT | Updates an existing calendar ACL rule in Google Calendar. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Add Calendar to List](actions/add-calendar-to-list.md) | POST | Adds an existing calendar to the Google Calendar list. |
| [Clear Calendar](actions/clear-calendar.md) | DELETE | Deletes all events from a primary Google Calendar. |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a secondary calendar in Google Calendar. |
| [Get Calendar List Entry](actions/get-calendar-list-entry.md) | GET | Retrieves a calendar list entry from Google Calendar. |
| [Get Calendar Metadata](actions/get-calendar-metadata.md) | GET | Retrieves calendar metadata from Google Calendar. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendar list entries from Google Calendar. |
| [Patch Calendar List Entry](actions/patch-calendar-list-entry.md) | PUT | Updates a calendar list entry in Google Calendar. |
| [Remove Calendar from List](actions/remove-calendar-from-list.md) | DELETE | Removes a calendar from the Google Calendar list. |
| [Update Calendar List Entry](actions/update-calendar-list-entry.md) | PUT | Updates an existing calendar list entry in Google Calendar. |

### Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Google Calendar. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Google Calendar. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Google Calendar. |
| [Import Event](actions/import-event.md) | POST | Imports a private event copy into Google Calendar. |
| [List Event Instances](actions/list-event-instances.md) | GET | Retrieves recurring event instances from Google Calendar. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Google Calendar calendar. |
| [Move Event](actions/move-event.md) | PUT | Moves an event to another calendar in Google Calendar. |
| [Quick Add Event](actions/quick-add-event.md) | POST | Creates an event from text in Google Calendar. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Google Calendar. |

### Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Colors](actions/get-colors.md) | GET | Retrieves calendar and event colors from Google Calendar. |

### Free Busy

| Action | Method | Description |
| --- | --- | --- |
| [Query Free/Busy](actions/query-free-busy.md) | GET | Retrieves free/busy information from Google Calendar. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Setting](actions/get-setting.md) | GET | Retrieves a calendar setting from Google Calendar. |
| [List Settings](actions/list-settings.md) | GET | Retrieves calendar settings from Google Calendar. |

