# Teamdeck: Native API Reference

A consolidated summary of Teamdeck's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://teamdeck.io/developers/api
- **API base URL:** `https://api.teamdeck.io/v1`

## Authentication

### API Key

Connect using a Teamdeck API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://teamdeck.io/developers/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Resource](actions/activate-resource.md) | `PUT /resources/:id/activate` | [docs](https://teamdeck.io/developers/api#operation/activateResource) |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://teamdeck.io/developers/api#operation/addBooking) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://teamdeck.io/developers/api#operation/addProject) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time-entries` | [docs](https://teamdeck.io/developers/api#operation/addTimeEntry) |
| [Create Vacation](actions/create-vacation.md) | `POST /vacations` | [docs](https://teamdeck.io/developers/api#operation/addVacations) |
| [Deactivate Resource](actions/deactivate-resource.md) | `PUT /resources/:id/deactivate` | [docs](https://teamdeck.io/developers/api#operation/deactivateResource) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /bookings/:id` | [docs](https://teamdeck.io/developers/api#operation/bookingDelete) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /time-entries/:id` | [docs](https://teamdeck.io/developers/api#operation/timeEntryDelete) |
| [Delete Vacation](actions/delete-vacation.md) | `DELETE /vacations/:id` | [docs](https://teamdeck.io/developers/api#operation/vacationDelete) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:id` | [docs](https://teamdeck.io/developers/api#operation/bookingDetails) |
| [Get Organization](actions/get-organization.md) | `GET /me` | [docs](https://teamdeck.io/developers/api#operation/me) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://teamdeck.io/developers/api#operation/projectDetails) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:id` | [docs](https://teamdeck.io/developers/api#operation/resourceDetails) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /time-entries/:id` | [docs](https://teamdeck.io/developers/api#operation/timeEntryDetails) |
| [Get Vacation](actions/get-vacation.md) | `GET /vacations/:id` | [docs](https://teamdeck.io/developers/api#operation/vacationDetails) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://teamdeck.io/developers/api#operation/bookingsList) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://teamdeck.io/developers/api#operation/projectsList) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://teamdeck.io/developers/api#operation/resourcesList) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time-entries` | [docs](https://teamdeck.io/developers/api#operation/timeEntriesList) |
| [List Vacations](actions/list-vacations.md) | `GET /vacations` | [docs](https://teamdeck.io/developers/api#operation/vacationsList) |
| [Update Booking](actions/update-booking.md) | `PUT /bookings/:id` | [docs](https://teamdeck.io/developers/api#operation/updateBooking) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://teamdeck.io/developers/api#operation/updateProject) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /time-entries/:id` | [docs](https://teamdeck.io/developers/api#operation/updateTimeEntry) |
| [Update Vacation](actions/update-vacation.md) | `PUT /vacations/:id` | [docs](https://teamdeck.io/developers/api#operation/updateVacation) |
