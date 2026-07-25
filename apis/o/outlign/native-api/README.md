# Outlign: Native API Reference

A consolidated summary of Outlign's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://go.outlign.co/api/docs
- **API base URL:** `https://go.outlign.co/api/v1`

## Authentication

### OAuth2

Connect your Outlign account with OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://go.outlign.co/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://go.outlign.co/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `outlign:all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://go.outlign.co/oauth/token.

[Official authentication documentation](https://go.outlign.co/api/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (maximum 1000).

## Filtering

Send filters in the query string.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://go.outlign.co/api/docs/clients) |
| [Create Internal Phase](actions/create-internal-phase.md) | `POST /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [Create Phase](actions/create-phase.md) | `POST /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [Create Task](actions/create-task.md) | `POST /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/:id` | [docs](https://go.outlign.co/api/docs/clients) |
| [Delete Task](actions/delete-task.md) | `DELETE /steps/:id` | [docs](https://go.outlign.co/api/docs/tasks) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://go.outlign.co/api/docs/clients) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://go.outlign.co/api/docs/authentication) |
| [Get Phase](actions/get-phase.md) | `GET /phases/:id` | [docs](https://go.outlign.co/api/docs/phases) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://go.outlign.co/api/docs/projects) |
| [Get Task](actions/get-task.md) | `GET /steps/:id` | [docs](https://go.outlign.co/api/docs/tasks) |
| [List Client-Facing Phases](actions/list-client-facing-phases.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://go.outlign.co/api/docs/clients) |
| [List Clients By Company](actions/list-clients-by-company.md) | `GET /clients` | [docs](https://go.outlign.co/api/docs/clients) |
| [List Clients by Company (Alternate)](actions/list-clients-by-company-alternate.md) | `GET /clients` | [docs](https://go.outlign.co/api/docs/clients) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://go.outlign.co/api/docs/companies) |
| [List Companies (Alternate Schema)](actions/list-companies-alternate-schema.md) | `GET /companies` | [docs](https://go.outlign.co/api/docs/companies) |
| [List Completed Tasks](actions/list-completed-tasks.md) | `GET /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [List Internal Phases](actions/list-internal-phases.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Milestones](actions/list-milestones.md) | `GET /milestones` | [docs](https://go.outlign.co/api/docs/milestones) |
| [List Non-Template Tasks](actions/list-non-template-tasks.md) | `GET /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [List Open Tasks](actions/list-open-tasks.md) | `GET /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [List Phases](actions/list-phases.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Phases By Client](actions/list-phases-by-client.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Phases By Company](actions/list-phases-by-company.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Phases By Project](actions/list-phases-by-project.md) | `GET /phases` | [docs](https://go.outlign.co/api/docs/phases) |
| [List Project Templates](actions/list-project-templates.md) | `GET /project-templates` | [docs](https://go.outlign.co/api/docs/project-templates) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://go.outlign.co/api/docs/projects) |
| [List Projects By Client](actions/list-projects-by-client.md) | `GET /projects` | [docs](https://go.outlign.co/api/docs/projects) |
| [List Projects by Client and Company](actions/list-projects-by-client-and-company.md) | `GET /projects` | [docs](https://go.outlign.co/api/docs/projects) |
| [List Projects By Company](actions/list-projects-by-company.md) | `GET /projects` | [docs](https://go.outlign.co/api/docs/projects) |
| [List Tasks](actions/list-tasks.md) | `GET /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [List Tasks With Due Dates](actions/list-tasks-with-due-dates.md) | `GET /steps` | [docs](https://go.outlign.co/api/docs/tasks) |
| [Mark Task Completed](actions/mark-task-completed.md) | `PUT /steps/:id` | [docs](https://go.outlign.co/api/docs/tasks) |
| [Search Clients By Title](actions/search-clients-by-title.md) | `GET /clients` | [docs](https://go.outlign.co/api/docs/clients) |
| [Search Projects By Title](actions/search-projects-by-title.md) | `GET /projects` | [docs](https://go.outlign.co/api/docs/projects) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://go.outlign.co/api/docs/clients) |
| [Update Task](actions/update-task.md) | `PUT /steps/:id` | [docs](https://go.outlign.co/api/docs/tasks) |
