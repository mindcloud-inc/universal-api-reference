# <img src="https://images.mindcloud.co/apps/icons/orufy-bookings_1774367487119.png" alt="Orufy Bookings logo" width="28" height="28"> Orufy Bookings: Universal API

Orufy Bookings is an online scheduling platform for creating booking pages, managing availability, sharing scheduling links, handling contacts, and coordinating meetings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orufyBookings/latest
- **Category:** Productivity / Scheduling
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orufy.com/bookings
- **Vendor API docs:** https://orufy.com/support/bookings

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | PUT |  |
| [Create Booking](actions/create-booking.md) | POST |  |
| [Reschedule Booking](actions/reschedule-booking.md) | PUT |  |
| [Validate Booking Slot](actions/validate-booking-slot.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET |  |
| [Get Public Event](actions/get-public-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |
| [List Public Events](actions/list-public-events.md) | GET |  |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Queue Status](actions/get-booking-queue-status.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Availability](actions/get-event-availability.md) | GET |  |

