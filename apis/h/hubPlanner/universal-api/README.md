# <img src="https://images.mindcloud.co/apps/icons/hub-planner_1776722887971.png" alt="Hub Planner logo" width="28" height="28"> Hub Planner: Universal API

Hub Planner, now part of Milient Resource Management, provides resource planning, project scheduling, bookings, timesheets, vacations, groups, clients, and related resource management data through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hubPlanner/latest
- **Category:** Productivity / Scheduling
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hubplanner.com
- **Vendor API docs:** https://github.com/hubplanner/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Booking Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Category](actions/get-booking-category.md) | GET | Retrieves a booking category from Hub Planner. |
| [List Booking Categories](actions/list-booking-categories.md) | GET | Retrieves booking categories from Hub Planner. |
| [Search Booking Categories](actions/search-booking-categories.md) | GET | Finds booking categories in Hub Planner by search criteria. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Hub Planner. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Hub Planner. |
| [Search Bookings](actions/search-bookings.md) | GET | Finds bookings in Hub Planner by search criteria. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Hub Planner. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Hub Planner. |
| [Search Clients](actions/search-clients.md) | GET | Finds clients in Hub Planner by search criteria. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Hub Planner. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Hub Planner. |
| [Search Events](actions/search-events.md) | GET | Finds events in Hub Planner by search criteria. |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Get Holiday](actions/get-holiday.md) | GET | Retrieves a holiday from Hub Planner. |
| [List Holidays](actions/list-holidays.md) | GET | Retrieves holidays from Hub Planner. |
| [Search Holidays](actions/search-holidays.md) | GET | Finds holidays in Hub Planner by search criteria. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Rate](actions/get-billing-rate.md) | GET | Retrieves a billing rate from Hub Planner. |
| [List Billing Rates](actions/list-billing-rates.md) | GET | Retrieves billing rates from Hub Planner. |
| [Search Billing Rates](actions/search-billing-rates.md) | GET | Finds billing rates in Hub Planner by search criteria. |

### Project Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Group](actions/get-project-group.md) | GET | Retrieves a project group from Hub Planner. |
| [List Project Groups](actions/list-project-groups.md) | GET | Retrieves project groups from Hub Planner. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Hub Planner. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Hub Planner. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Hub Planner by search criteria. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Hub Planner. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from Hub Planner. |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in Hub Planner by search criteria. |

### Resource Group

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Groups](actions/list-resource-groups.md) | GET | Retrieves resource groups from Hub Planner. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Hub Planner. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Hub Planner. |
| [Search Time Entries](actions/search-time-entries.md) | GET | Finds time entries in Hub Planner by search criteria. |

