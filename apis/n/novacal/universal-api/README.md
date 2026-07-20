# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-novacal-io-48x48_1778172727466.png" alt="Novacal logo" width="28" height="28"> Novacal: Universal API

Novacal is a scheduling and booking platform for managing event types, availability, bookings, teams, booking forms, and user profile settings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/novacal/latest
- **Category:** Productivity / Scheduling
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.novacal.io/
- **Vendor API docs:** https://docs.novacal.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Availability](actions/get-availability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Book Event](actions/book-event.md) | POST | Creates a new event booking in Novacal. |
| [Cancel Event](actions/cancel-event.md) | PUT | Cancels an existing event in Novacal. |
| [Get Event](actions/get-event.md) | GET | Retrieves event details from Novacal. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Novacal. |
| [Reschedule Event](actions/reschedule-event.md) | PUT | Updates an existing event in Novacal. |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves availability from Novacal. |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Type](actions/create-event-type.md) | POST | Creates a new event type in Novacal. |
| [Delete Event Type](actions/delete-event-type.md) | DELETE | Deletes an existing event type from Novacal. |
| [Get Event Type](actions/get-event-type.md) | GET | Retrieves event type details from Novacal. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types from Novacal. |
| [Update Event Type](actions/update-event-type.md) | PUT | Updates an existing event type in Novacal. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking Form Field](actions/create-booking-form-field.md) | POST | Creates a new booking form field in Novacal. |
| [Delete Booking Form Field](actions/delete-booking-form-field.md) | DELETE | Deletes an existing booking form field from Novacal. |
| [List Booking Form Fields](actions/list-booking-form-fields.md) | GET | Retrieves booking form fields from Novacal. |
| [Update Booking Form Field](actions/update-booking-form-field.md) | PUT | Updates an existing booking form field in Novacal. |
| [Update Booking Form Field Order](actions/update-booking-form-field-order.md) | PUT | Updates booking form field order in Novacal. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves team details from Novacal. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Novacal. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Novacal. |
| [Update Current User](actions/update-current-user.md) | PUT | Updates the current user in Novacal. |

