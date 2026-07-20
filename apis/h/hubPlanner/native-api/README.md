# Hub Planner: Native API Reference

A consolidated summary of Hub Planner's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://github.com/hubplanner/API
- **API base URL:** `https://api.hubplanner.com/v1`

## Authentication

### API Key

Use a Hub Planner API key generated from Settings > API. Hub Planner requires the raw key in the Authorization header without a Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://github.com/hubplanner/API#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Hub Planner Integration (apps@mindcloud.co)` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Billing Rate](actions/get-billing-rate.md) | `GET /billingRate/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/billingrate.md#get-specific-billing-rate) |
| [Get Booking](actions/get-booking.md) | `GET /booking/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/bookings.md#get-specific-booking) |
| [Get Booking Category](actions/get-booking-category.md) | `GET /categories/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/booking-categories.md#get-a-booking-category-by-id) |
| [Get Client](actions/get-client.md) | `GET /client/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/clients.md#get-an-existing-client) |
| [Get Event](actions/get-event.md) | `GET /event/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/events.md#get-specific-event) |
| [Get Holiday](actions/get-holiday.md) | `GET /holiday/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/holidays.md#get-specific-holidays) |
| [Get Project](actions/get-project.md) | `GET /project/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/project.md#get-specific-project) |
| [Get Project Group](actions/get-project-group.md) | `GET /projectgroup/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/groups.md#get-specific-project) |
| [Get Resource](actions/get-resource.md) | `GET /resource/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/resource.md#get-specific-resource) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /timeentry/:id` | [docs](https://github.com/hubplanner/API/blob/master/Sections/timesheets.md#get-specific-timeentry) |
| [List Billing Rates](actions/list-billing-rates.md) | `GET /billingRate` | [docs](https://github.com/hubplanner/API/blob/master/Sections/billingrate.md#get-all-billing-rates) |
| [List Booking Categories](actions/list-booking-categories.md) | `GET /categories` | [docs](https://github.com/hubplanner/API/blob/master/Sections/booking-categories.md#get-all-booking-categories) |
| [List Bookings](actions/list-bookings.md) | `GET /booking` | [docs](https://github.com/hubplanner/API/blob/master/Sections/bookings.md#get-all-bookings) |
| [List Clients](actions/list-clients.md) | `GET /client` | [docs](https://github.com/hubplanner/API/blob/master/Sections/clients.md#get-all-clients) |
| [List Events](actions/list-events.md) | `GET /event` | [docs](https://github.com/hubplanner/API/blob/master/Sections/events.md#add-events-to-resources) |
| [List Holidays](actions/list-holidays.md) | `GET /holiday` | [docs](https://github.com/hubplanner/API/blob/master/Sections/holidays.md#get-all-holidays) |
| [List Project Groups](actions/list-project-groups.md) | `GET /projectgroup` | [docs](https://github.com/hubplanner/API/blob/master/Sections/groups.md#get-all-project-or-resource-groups) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://github.com/hubplanner/API/blob/master/Sections/project.md#get-all-projects) |
| [List Resource Groups](actions/list-resource-groups.md) | `GET /resourcegroup` | [docs](https://github.com/hubplanner/API/blob/master/Sections/groups.md#get-all-project-or-resource-groups) |
| [List Resources](actions/list-resources.md) | `GET /resource` | [docs](https://github.com/hubplanner/API/blob/master/Sections/resource.md#get-all-resources) |
| [List Time Entries](actions/list-time-entries.md) | `GET /timeentry` | [docs](https://github.com/hubplanner/API/blob/master/Sections/timesheets.md#get-all-time-entries) |
| [Search Billing Rates](actions/search-billing-rates.md) | `POST /billingRate/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/billingrate.md#search-billing-rates) |
| [Search Booking Categories](actions/search-booking-categories.md) | `POST /categories/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/booking-categories.md#search-a-booking-category) |
| [Search Bookings](actions/search-bookings.md) | `POST /booking/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/bookings.md#search-bookings) |
| [Search Clients](actions/search-clients.md) | `POST /client/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/clients.md#search-clients) |
| [Search Events](actions/search-events.md) | `POST /event/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/events.md#search-events) |
| [Search Holidays](actions/search-holidays.md) | `POST /holiday/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/holidays.md#search-holidays) |
| [Search Projects](actions/search-projects.md) | `POST /project/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/project.md#search-projects) |
| [Search Resources](actions/search-resources.md) | `POST /resource/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/resource.md#search-resources) |
| [Search Time Entries](actions/search-time-entries.md) | `POST /timeentry/search` | [docs](https://github.com/hubplanner/API/blob/master/Sections/timesheets.md#search-timeentry) |
