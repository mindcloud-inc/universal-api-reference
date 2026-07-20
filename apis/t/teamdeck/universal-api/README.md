# <img src="https://images.mindcloud.co/apps/icons/teamdesk-icon_1775769375264.png" alt="Teamdeck logo" width="28" height="28"> Teamdeck: Universal API

Manage resources, projects, bookings, time entries, and vacations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamdeck/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teamdeck.io
- **Vendor API docs:** https://teamdeck.io/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Teamdeck. |
| [Delete Booking](actions/delete-booking.md) | DELETE | Deletes an existing booking from Teamdeck. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from your Teamdeck organization. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from your Teamdeck organization. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in Teamdeck. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves your organization details from Teamdeck. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Teamdeck. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your Teamdeck organization. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Teamdeck organization. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Teamdeck. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Activate Resource](actions/activate-resource.md) | PUT | Activates an existing resource in Teamdeck. |
| [Deactivate Resource](actions/deactivate-resource.md) | PUT | Deactivates an existing resource in Teamdeck. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from your Teamdeck organization. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from your Teamdeck organization. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Teamdeck. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Teamdeck. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from your Teamdeck organization. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from your Teamdeck organization. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Teamdeck. |

### Vacation

| Action | Method | Description |
| --- | --- | --- |
| [Create Vacation](actions/create-vacation.md) | POST | Creates a new vacation in Teamdeck. |
| [Delete Vacation](actions/delete-vacation.md) | DELETE | Deletes an existing vacation from Teamdeck. |
| [Get Vacation](actions/get-vacation.md) | GET | Retrieves a vacation from your Teamdeck organization. |
| [List Vacations](actions/list-vacations.md) | GET | Retrieves vacations from your Teamdeck organization. |
| [Update Vacation](actions/update-vacation.md) | PUT | Updates an existing vacation in Teamdeck. |

