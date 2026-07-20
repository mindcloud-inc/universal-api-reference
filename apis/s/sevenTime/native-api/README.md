# Seven Time: Native API Reference

A consolidated summary of Seven Time's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.seventime.se
- **API base URL:** `https://app.seventime.se/api/2`

## Authentication

### API Key

Use a Seven Time API key in the Client-Secret header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Client-Secret: <apiKey>
```

[Official authentication documentation](https://docs.seventime.se/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.totalPages`. The current page number is read from `meta.currentPage`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `ascending` for ascending order and `descending` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User](actions/get-user.md) | `GET /users/:_id` | [docs](https://docs.seventime.se/#get-a-specific-user) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.seventime.se/#get-customers) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://docs.seventime.se/#get-departments) |
| [List Invoice Tags](actions/list-invoice-tags.md) | `GET /invoiceTags` | [docs](https://docs.seventime.se/#get-invoice-tags) |
| [List Machine Types](actions/list-machine-types.md) | `GET /machineTypes` | [docs](https://docs.seventime.se/#get-machine-types) |
| [List Price Lists](actions/list-price-lists.md) | `GET /priceLists` | [docs](https://docs.seventime.se/#get-price-lists) |
| [List Project Statuses](actions/list-project-statuses.md) | `GET /projectStatuses` | [docs](https://docs.seventime.se/#get-project-statuses) |
| [List Project Tags](actions/list-project-tags.md) | `GET /projectTags` | [docs](https://docs.seventime.se/#get-project-tags) |
| [List Project Types](actions/list-project-types.md) | `GET /projectTypes` | [docs](https://docs.seventime.se/#get-project-types) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.seventime.se/#get-projects) |
| [List Quote Categories](actions/list-quote-categories.md) | `GET /quoteCategories` | [docs](https://docs.seventime.se/#get-quote-categories) |
| [List Quote Templates](actions/list-quote-templates.md) | `GET /quoteTemplates` | [docs](https://docs.seventime.se/#get-quote-templates) |
| [List Result Units](actions/list-result-units.md) | `GET /resultUnits` | [docs](https://docs.seventime.se/#get-result-units) |
| [List Time Categories](actions/list-time-categories.md) | `GET /timeCategories` | [docs](https://docs.seventime.se/#get-time-categories) |
| [List Time Logs](actions/list-time-logs.md) | `GET /timeLogs` | [docs](https://docs.seventime.se/#get-time-logs) |
| [List User Roles](actions/list-user-roles.md) | `GET /userRoles` | [docs](https://docs.seventime.se/#get-user-roles) |
| [List User Salary Types](actions/list-user-salary-types.md) | `GET /defaultSalaryTypes` | [docs](https://docs.seventime.se/#get-user-salary-types) |
| [List User Skills](actions/list-user-skills.md) | `GET /userSkills` | [docs](https://docs.seventime.se/#get-user-skills) |
| [List User Work Types](actions/list-user-work-types.md) | `GET /userWorkTypes` | [docs](https://docs.seventime.se/#get-user-work-types) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.seventime.se/#get-users) |
| [List Work Order Statuses](actions/list-work-order-statuses.md) | `GET /workOrderStatuses` | [docs](https://docs.seventime.se/#get-work-order-statuses) |
| [List Work Order Tags](actions/list-work-order-tags.md) | `GET /workOrderTags` | [docs](https://docs.seventime.se/#get-work-order-tags) |
| [List Work Order Types](actions/list-work-order-types.md) | `GET /workOrderTypes` | [docs](https://docs.seventime.se/#get-work-order-types) |
| [List Work Schedules](actions/list-work-schedules.md) | `GET /workSchedules` | [docs](https://docs.seventime.se/#get-work-schedules) |
