# <img src="https://images.mindcloud.co/apps/icons/calendar-link_1774640686518.png" alt="CalendarLink logo" width="28" height="28"> CalendarLink: Universal API

Create and share calendar links, subscription calendars, and RSVPs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calendarLink/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calendarlink.com
- **Vendor API docs:** https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from a CalendarLink organization. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from a CalendarLink organization. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a CalendarLink organization. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in a CalendarLink organization. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from a CalendarLink organization. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a CalendarLink organization. |
| [List Past Events](actions/list-past-events.md) | GET | Retrieves past events from a CalendarLink organization. |

### Event Registration

| Action | Method | Description |
| --- | --- | --- |
| [List Event Registrations](actions/list-event-registrations.md) | GET | Retrieves event registrations from a CalendarLink event. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from CalendarLink. |

