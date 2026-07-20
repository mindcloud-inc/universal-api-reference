# <img src="https://images.mindcloud.co/apps/icons/timekit_1774366632157.png" alt="Timekit logo" width="28" height="28"> Timekit: Universal API

Empower your customers to book your team and grow your business with automated scheduling.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timekit/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.timekit.io/
- **Vendor API docs:** https://developers.timekit.io/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current App](actions/get-current-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/get-current-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Get Current App](actions/get-current-app.md) | GET | Retrieves the current app from Timekit. |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability Counts](actions/get-availability-counts.md) | GET | Retrieves available timeslot counts from Timekit. |
| [Get Availability Dates](actions/get-availability-dates.md) | GET | Retrieves available booking dates from Timekit. |
| [Get Unavailable Slots](actions/get-unavailable-slots.md) | GET | Retrieves unavailable booking timeslots from Timekit. |
| [Query Availability](actions/query-availability.md) | GET | Finds available booking timeslots in Timekit. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Timekit. |
| [Delete Booking](actions/delete-booking.md) | DELETE | Deletes an existing booking from Timekit. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves details for a booking from Timekit. |
| [List Bookings](actions/list-bookings.md) | GET | Lists all existing bookings in Timekit. |
| [Reschedule Booking](actions/reschedule-booking.md) | PUT |  |
| [Update Booking Meta](actions/update-booking-meta.md) | PUT | Updates metadata for a booking in Timekit. |
| [Update Booking State](actions/update-booking-state.md) | PUT | Updates a booking's state in Timekit. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Lists all available locations in Timekit. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Resource](actions/add-project-resource.md) | PUT | Adds a resource to a project in Timekit. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Timekit. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Timekit. |
| [List Project Resources](actions/list-project-resources.md) | GET | Lists resources for a project in Timekit. |
| [List Projects](actions/list-projects.md) | GET | Lists all scheduling projects in Timekit. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Timekit. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Timekit. |
| [Delete Resource](actions/delete-resource.md) | DELETE | Deletes an existing resource from Timekit. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves details for a resource from Timekit. |
| [List Resources](actions/list-resources.md) | GET | Lists all available resources in Timekit. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Timekit. |

