# Craftboxx: Native API Reference

A consolidated summary of Craftboxx's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://api.craftboxx.de/
- **OpenAPI specification:** https://api.craftboxx.de/docs?api-docs.json
- **API base URL:** `https://api.craftboxx.de`

## Authentication

### Employee Login

Authenticate with a Craftboxx employee login to exchange email and password for a bearer access token.

### Credentials

- **Email:** `email` · required · Craftboxx employee email address used to create a bearer token.
- **Password:** `password` · required · Craftboxx employee password used to create a bearer token.

[Official authentication documentation](https://api.craftboxx.de/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Assignment Availability](actions/check-assignment-availability.md) | `GET assignments/check-availability` | [docs](https://api.craftboxx.de/) |
| [Create Access Token](actions/create-access-token.md) | `POST auth/create-token` | [docs](https://api.craftboxx.de/) |
| [Create Article](actions/create-article.md) | `POST articles` | [docs](https://api.craftboxx.de/) |
| [Create Assignment](actions/create-assignment.md) | `POST assignments` | [docs](https://api.craftboxx.de/) |
| [Create Customer](actions/create-customer.md) | `POST customers` | [docs](https://api.craftboxx.de/) |
| [Create Employee](actions/create-employee.md) | `POST employees` | [docs](https://api.craftboxx.de/) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://api.craftboxx.de/) |
| [Create Timesheet](actions/create-timesheet.md) | `POST timesheets` | [docs](https://api.craftboxx.de/) |
| [Get Article](actions/get-article.md) | `GET articles/:articleId` | [docs](https://api.craftboxx.de/) |
| [Get Assignment](actions/get-assignment.md) | `GET assignments/:assignmentId` | [docs](https://api.craftboxx.de/) |
| [Get Customer](actions/get-customer.md) | `GET customers/:customerId` | [docs](https://api.craftboxx.de/) |
| [Get Employee](actions/get-employee.md) | `GET employees/:employeeId` | [docs](https://api.craftboxx.de/) |
| [Get Project](actions/get-project.md) | `GET projects/:projectId` | [docs](https://api.craftboxx.de/) |
| [Get Timesheet](actions/get-timesheet.md) | `GET timesheets/:timesheetId` | [docs](https://api.craftboxx.de/) |
| [List Articles](actions/list-articles.md) | `GET articles` | [docs](https://api.craftboxx.de/) |
| [List Assignments](actions/list-assignments.md) | `GET assignments` | [docs](https://api.craftboxx.de/) |
| [List Customers](actions/list-customers.md) | `GET customers` | [docs](https://api.craftboxx.de/) |
| [List Employees](actions/list-employees.md) | `GET employees` | [docs](https://api.craftboxx.de/) |
| [List Projects](actions/list-projects.md) | `GET projects` | [docs](https://api.craftboxx.de/) |
| [List Timesheets](actions/list-timesheets.md) | `GET timesheets` | [docs](https://api.craftboxx.de/) |
| [Update Article](actions/update-article.md) | `PUT articles/:articleId` | [docs](https://api.craftboxx.de/) |
| [Update Assignment](actions/update-assignment.md) | `PUT assignments/:assignmentId` | [docs](https://api.craftboxx.de/) |
| [Update Customer](actions/update-customer.md) | `PUT customers/:customerId` | [docs](https://api.craftboxx.de/) |
| [Update Employee](actions/update-employee.md) | `PUT employees/:employeeId` | [docs](https://api.craftboxx.de/) |
| [Update Project](actions/update-project.md) | `PUT projects/:projectId` | [docs](https://api.craftboxx.de/) |
| [Update Timesheet](actions/update-timesheet.md) | `PUT timesheets/:timesheetId` | [docs](https://api.craftboxx.de/) |
