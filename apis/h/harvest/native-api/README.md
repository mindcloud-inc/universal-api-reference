# Harvest: Native API Reference

A consolidated summary of Harvest's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://help.getharvest.com/api-v2/
- **API base URL:** `https://api.harvestapp.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://id.getharvest.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://id.getharvest.com/api/v2/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://id.getharvest.com/api/v2/oauth2/token.

[Official authentication documentation](https://help.getharvest.com/api-v2/authentication-api/authentication/authentication/)

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.getharvest.com/api-v2/authentication-api/authentication/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud (apps@mindcloud.co)` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 2000; accepted range 1–2000). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /v2/clients` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/clients/) |
| [Create Contact](actions/create-contact.md) | `POST /v2/contacts` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/contacts/) |
| [Create Expense](actions/create-expense.md) | `POST /v2/expenses` | [docs](https://help.getharvest.com/api-v2/expenses-api/expenses/expenses/) |
| [Create Invoice](actions/create-invoice.md) | `POST /v2/invoices` | [docs](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/) |
| [Create Project](actions/create-project.md) | `POST /v2/projects` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/projects/) |
| [Create Project Task Assignment](actions/create-project-task-assignment.md) | `POST /v2/projects/:projectId/task_assignments` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/task-assignments/) |
| [Create Task](actions/create-task.md) | `POST /v2/tasks` | [docs](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /v2/time_entries` | [docs](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/) |
| [Delete client](actions/delete-client.md) | `DELETE /v2/clients/:id` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/clients/) |
| [Delete invoice](actions/delete-invoice.md) | `DELETE /v2/invoices/:id` | [docs](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/) |
| [Delete project](actions/delete-project.md) | `DELETE /v2/projects/:id` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/projects/) |
| [Delete task](actions/delete-task.md) | `DELETE /v2/tasks/:id` | [docs](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/) |
| [List Clients](actions/list-clients.md) | `GET /v2/clients` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/clients/) |
| [List Contacts](actions/list-contacts.md) | `GET /v2/contacts` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/contacts/) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET /v2/expense_categories` | [docs](https://help.getharvest.com/api-v2/expenses-api/expenses/expense-categories/) |
| [List Expenses](actions/list-expenses.md) | `GET /v2/expenses` | [docs](https://help.getharvest.com/api-v2/expenses-api/expenses/expenses/) |
| [List Invoices](actions/list-invoices.md) | `GET /v2/invoices` | [docs](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/) |
| [List Projects](actions/list-projects.md) | `GET /v2/projects` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/projects/) |
| [List Tasks](actions/list-tasks.md) | `GET /v2/tasks` | [docs](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/) |
| [List Time Entries](actions/list-time-entries.md) | `GET /v2/time_entries` | [docs](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/) |
| [List Users](actions/list-users.md) | `GET /v2/users` | [docs](https://help.getharvest.com/api-v2/users-api/users/users/) |
| [Retrieve Client](actions/retrieve-client.md) | `GET /v2/clients/:id` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/clients/) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /v2/company` | [docs](https://help.getharvest.com/api-v2/company-api/company/company/) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /v2/contacts/:id` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/contacts/) |
| [Retrieve Current User](actions/retrieve-current-user.md) | `GET /v2/users/me` | [docs](https://help.getharvest.com/api-v2/users-api/users/users/) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /v2/invoices/:id` | [docs](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /v2/projects/:id` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/projects/) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /v2/tasks/:id` | [docs](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/) |
| [Retrieve Time Entry](actions/retrieve-time-entry.md) | `GET /v2/time_entries/:id` | [docs](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/) |
| [Update Client](actions/update-client.md) | `PATCH /v2/clients/:id` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/clients/) |
| [Update Contact](actions/update-contact.md) | `PATCH /v2/contacts/:id` | [docs](https://help.getharvest.com/api-v2/clients-api/clients/contacts/) |
| [Update Expense](actions/update-expense.md) | `PATCH /v2/expenses/:id` | [docs](https://help.getharvest.com/api-v2/expenses-api/expenses/expenses/) |
| [Update Invoice](actions/update-invoice.md) | `PATCH /v2/invoices/:id` | [docs](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/) |
| [Update Project](actions/update-project.md) | `PATCH /v2/projects/:id` | [docs](https://help.getharvest.com/api-v2/projects-api/projects/projects/) |
| [Update Task](actions/update-task.md) | `PATCH /v2/tasks/:id` | [docs](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/) |
| [Update Time Entry](actions/update-time-entry.md) | `PATCH /v2/time_entries/:id` | [docs](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/) |
