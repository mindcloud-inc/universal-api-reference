# <img src="https://images.mindcloud.co/apps/icons/team-up_1773670692454.png" alt="TeamUp logo" width="28" height="28"> TeamUp: Universal API

Manage calendar events and scheduling

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamUp/latest
- **Category:** Productivity / Scheduling
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teamup.com/
- **Vendor API docs:** https://apidocs.teamup.com/docs/api/f835b6c908790-teamup-com-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Calendar Configuration](actions/get-calendar-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in TeamUp. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from TeamUp. |
| [Get Event](actions/get-event.md) | GET | Retrieves a single event from TeamUp. |
| [Get Event Page URL](actions/get-event-page-url.md) | GET | Retrieves the page URL for a TeamUp event. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a TeamUp calendar by date range. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in TeamUp. |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Configuration](actions/get-calendar-configuration.md) | GET | Retrieves configuration for a TeamUp calendar. |

