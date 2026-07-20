# <img src="https://images.mindcloud.co/apps/icons/flexopus_1775654896119.png" alt="Flexopus logo" width="28" height="28"> Flexopus: Universal API

Flexopus: Manage workplace bookings, resources, events, and occupancy

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flexopus/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flexopus.com
- **Vendor API docs:** https://flexopus.com/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buildings](actions/list-buildings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Flexopus. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Flexopus. |
| [Get Event](actions/get-event.md) | GET | Retrieves a specific event from Flexopus. |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from Flexopus. |
| [List Today's Events](actions/list-todays-events.md) | GET | Retrieves today's events from a Flexopus account. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Flexopus. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Flexopus. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Buildings](actions/list-buildings.md) | GET | Retrieves a list of buildings from Flexopus. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Flexopus. |
| [Delete Booking](actions/delete-booking.md) | DELETE | Deletes an existing booking from Flexopus. |
| [List Bookable Bookings](actions/list-bookable-bookings.md) | GET | Retrieves bookings for a specific Flexopus bookable. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves a list of bookings from Flexopus. |
| [List Building Bookings](actions/list-building-bookings.md) | GET | Retrieves bookings for a specific Flexopus building. |
| [List Location Bookings](actions/list-location-bookings.md) | GET | Retrieves bookings for a specific Flexopus location. |
| [List User Bookings](actions/list-user-bookings.md) | GET | Retrieves bookings for a specific Flexopus user. |
| [List User Bookings by Email](actions/list-user-bookings-by-email.md) | GET | Retrieves bookings for a Flexopus user by email. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in Flexopus. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Export Users](actions/export-users.md) | GET | Retrieves a user export from Flexopus. |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from Flexopus. |
| [Get User by Email](actions/get-user-by-email.md) | GET | Retrieves a Flexopus user by email address. |
| [Import Users](actions/import-users.md) | POST | Imports users into Flexopus from a file. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Location Bookable Occupancy](actions/list-location-bookable-occupancy.md) | GET | Retrieves bookable occupancy for a Flexopus location. |
| [List Location Bookables](actions/list-location-bookables.md) | GET | Retrieves bookables for a specific Flexopus location. |
| [Update Bookable](actions/update-bookable.md) | PUT | Updates an existing bookable in Flexopus. |

