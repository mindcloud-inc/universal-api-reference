# <img src="https://images.mindcloud.co/apps/icons/calcom_1773090900010.png" alt="Cal.com logo" width="28" height="28"> Cal.com: Universal API

Manage bookings, event types, schedules, and availability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cal/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cal.com
- **Vendor API docs:** https://cal.com/docs/api-reference/v2/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bookings](actions/list-bookings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Add Booking Attendee](actions/add-booking-attendee.md) | PUT | Updates a booking in Cal.com by adding an attendee. |
| [Add Booking Guests](actions/add-booking-guests.md) | PUT | Updates a booking in Cal.com by adding guests. |
| [Cancel Booking](actions/cancel-booking.md) | PUT | Updates a booking in Cal.com by canceling it. |
| [Confirm Booking](actions/confirm-booking.md) | PUT | Updates a booking in Cal.com by confirming it. |
| [Create Booking](actions/create-booking.md) | POST | Creates a booking in Cal.com. |
| [Decline Booking](actions/decline-booking.md) | PUT | Updates a booking in Cal.com by declining it. |
| [Delete Reserved Slot](actions/delete-reserved-slot.md) | DELETE | Deletes a reserved slot from Cal.com. |
| [Get Available Slots](actions/get-available-slots.md) | GET | Retrieves available slots from Cal.com. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Cal.com. |
| [Get Reserved Slot](actions/get-reserved-slot.md) | GET | Retrieves a reserved slot from Cal.com. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Cal.com. |
| [Reschedule Booking](actions/reschedule-booking.md) | PUT | Updates a booking in Cal.com by rescheduling it. |
| [Reserve Slot](actions/reserve-slot.md) | POST | Creates a slot reservation in Cal.com. |
| [Update Booking Location](actions/update-booking-location.md) | PUT | Updates a booking location in Cal.com. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Type](actions/create-event-type.md) | POST | Creates an event type in Cal.com. |
| [Delete Event Type](actions/delete-event-type.md) | DELETE | Deletes an event type from Cal.com. |
| [Get Event Type](actions/get-event-type.md) | GET | Retrieves an event type from Cal.com. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types from Cal.com. |
| [Update Event Type](actions/update-event-type.md) | PUT | Updates an event type in Cal.com. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a schedule in Cal.com. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes a schedule from Cal.com. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves a schedule from Cal.com. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Cal.com. |
| [Update Schedule](actions/update-schedule.md) | PUT | Updates a schedule in Cal.com. |

