# <img src="https://images.mindcloud.co/apps/icons/add-cal_1774550196819.png" alt="AddCal logo" width="28" height="28"> AddCal: Universal API

AddCal: Create and manage calendar events, calendars, and RSVPs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/addCal/latest
- **Category:** Productivity / Scheduling
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://addcal.co
- **Vendor API docs:** https://addcal.co/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addCal/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Create Event RSVP](actions/create-event-rsvp.md) | POST | Creates an RSVP for a specific AddCal event. |
| [Delete Event RSVP](actions/delete-event-rsvp.md) | DELETE | Deletes an RSVP from a specific AddCal event. |
| [Get Event RSVP](actions/get-event-rsvp.md) | GET | Retrieves an RSVP from a specific AddCal event. |
| [List Event RSVPs](actions/list-event-rsvps.md) | GET | Retrieves RSVPs for a specific AddCal event. |
| [Update Event RSVP](actions/update-event-rsvp.md) | PUT | Updates an RSVP for a specific AddCal event. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in AddCal. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from AddCal. |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar from AddCal. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from AddCal. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in AddCal. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Event](actions/create-calendar-event.md) | POST | Creates an event in a specific AddCal calendar. |
| [Create Event](actions/create-event.md) | POST | Creates an event in AddCal with smart calendar defaults. |
| [Delete Calendar Event](actions/delete-calendar-event.md) | DELETE | Deletes an event from a specific AddCal calendar. |
| [Get Calendar Event](actions/get-calendar-event.md) | GET | Retrieves an event from a specific AddCal calendar. |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves events from a specific AddCal calendar. |
| [List Events](actions/list-events.md) | GET | Retrieves events from AddCal. |
| [Update Calendar Event](actions/update-calendar-event.md) | PUT | Updates an event in a specific AddCal calendar. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from AddCal. |

