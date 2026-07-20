# <img src="https://images.mindcloud.co/apps/icons/add-event_1773432764545.png" alt="AddEvent logo" width="28" height="28"> AddEvent: Universal API

Create, manage, and search events, calendars, RSVPs, and subscribers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/addEvent/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.addevent.com
- **Vendor API docs:** https://docs.addevent.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search calendars](actions/search-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create calendar](actions/create-calendar.md) | POST |  |
| [Delete calendar](actions/delete-calendar.md) | DELETE |  |
| [Retrieve calendar](actions/retrieve-calendar.md) | GET |  |
| [Search calendars](actions/search-calendars.md) | GET |  |
| [Update calendar](actions/update-calendar.md) | PUT |  |

### Calendar Template

| Action | Method | Description |
| --- | --- | --- |
| [List calendar templates](actions/list-calendar-templates.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create event](actions/create-event.md) | POST |  |
| [Delete event](actions/delete-event.md) | DELETE |  |
| [Retrieve event](actions/retrieve-event.md) | GET |  |
| [Search events](actions/search-events.md) | GET |  |
| [Update event](actions/update-event.md) | PUT |  |

### Event Template

| Action | Method | Description |
| --- | --- | --- |
| [List event templates](actions/list-event-templates.md) | GET |  |

### Rsvp Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Create RSVP attendee](actions/create-rsvp-attendee.md) | POST |  |
| [Delete RSVP attendee](actions/delete-rsvp-attendee.md) | DELETE |  |
| [Retrieve RSVP attendee](actions/retrieve-rsvp-attendee.md) | GET |  |
| [Search RSVP attendees](actions/search-rsvp-attendees.md) | GET |  |
| [Update RSVP attendee](actions/update-rsvp-attendee.md) | PUT |  |

### Rsvp Form

| Action | Method | Description |
| --- | --- | --- |
| [List RSVP forms](actions/list-rsvp-forms.md) | GET |  |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Delete calendar subscriber](actions/delete-calendar-subscriber.md) | DELETE |  |
| [Retrieve calendar subscriber](actions/retrieve-calendar-subscriber.md) | GET |  |
| [Search calendar subscribers](actions/search-calendar-subscribers.md) | GET |  |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List timezones](actions/list-timezones.md) | GET |  |

