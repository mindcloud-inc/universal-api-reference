# Timekit: Native API Reference

A consolidated summary of Timekit's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.timekit.io/reference/getting-started
- **API base URL:** `https://api.timekit.io/v2`

## Authentication

### Basic

Use HTTP Basic auth over HTTPS with an empty username and your Timekit App API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.timekit.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Resource](actions/add-project-resource.md) | `POST /projects/:id/resources` | [docs](https://developers.timekit.io/reference/add-resource-to-a-project) |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://developers.timekit.io/reference/bookings) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.timekit.io/reference/projects-1) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://developers.timekit.io/reference/resources) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /bookings/:id` | [docs](https://developers.timekit.io/reference/delete-a-booking) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://developers.timekit.io/reference/projectsid-2) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /resources/:id` | [docs](https://developers.timekit.io/reference/delete-resource) |
| [Get Availability Counts](actions/get-availability-counts.md) | `POST /availability/count` | [docs](https://developers.timekit.io/reference/availabilitycount) |
| [Get Availability Dates](actions/get-availability-dates.md) | `POST /availability/dates` | [docs](https://developers.timekit.io/reference/availabilitydates) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:id` | [docs](https://developers.timekit.io/reference/bookingsid) |
| [Get Current App](actions/get-current-app.md) | `GET /app` | [docs](https://developers.timekit.io/reference/app) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:id` | [docs](https://developers.timekit.io/reference/resourcesid) |
| [Get Unavailable Slots](actions/get-unavailable-slots.md) | `POST /unavailable/slots` | [docs](https://developers.timekit.io/reference/unavailable-slots) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://developers.timekit.io/reference/bookings-2) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developers.timekit.io/reference/list-all-locations) |
| [List Project Resources](actions/list-project-resources.md) | `GET /projects/:id/resources` | [docs](https://developers.timekit.io/reference/get-a-projects-resources) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.timekit.io/reference/projects) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://developers.timekit.io/reference/resources-1) |
| [Query Availability](actions/query-availability.md) | `POST /availability` | [docs](https://developers.timekit.io/reference/query-availability-v2) |
| [Reschedule Booking](actions/reschedule-booking.md) | `POST /bookings/:id/reschedule` | [docs](https://developers.timekit.io/reference/reschedule-a-booking) |
| [Update Booking Meta](actions/update-booking-meta.md) | `PUT /bookings/:id` | [docs](https://developers.timekit.io/reference/update-booking-meta-data) |
| [Update Booking State](actions/update-booking-state.md) | `PUT /bookings/:id/:action` | [docs](https://developers.timekit.io/reference/bookingsidaction) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://developers.timekit.io/reference/update-a-project) |
| [Update Resource](actions/update-resource.md) | `PUT /resources/:id` | [docs](https://developers.timekit.io/reference/resources-id) |
