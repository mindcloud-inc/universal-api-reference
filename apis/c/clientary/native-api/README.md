# Clientary: Native API Reference

A consolidated summary of Clientary's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.clientary.com/api
- **API base URL:** `https://{subdomain}.clientary.com/api/v2`

## Authentication

### API Token (Basic Auth)

Use your Clientary API token as both username and password, plus your account subdomain.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Subdomain:** `subdomain` · required · Your Clientary account subdomain, the part before .clientary.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.clientary.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `clients`. The total page count is read from `page_count`.

## Pagination

Use `page_size` in the query string to set the page size (maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://www.clientary.com/api/clients) |
| [Create Contact](actions/create-contact.md) | `POST /clients/:client_id/contacts` | [docs](https://www.clientary.com/api/contacts) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://www.clientary.com/api/estimates) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.clientary.com/api/invoices) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://www.clientary.com/api/projects) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://www.clientary.com/api/tasks) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://www.clientary.com/api/clients) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://www.clientary.com/api/contacts) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:id` | [docs](https://www.clientary.com/api/estimates) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://www.clientary.com/api/invoices) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://www.clientary.com/api/projects) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://www.clientary.com/api/tasks) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://www.clientary.com/api/clients) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.clientary.com/api/contacts) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://www.clientary.com/api/estimates) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.clientary.com/api/invoices) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.clientary.com/api/projects) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://www.clientary.com/api/tasks) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://www.clientary.com/api/clients) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://www.clientary.com/api/contacts) |
| [Update Estimate](actions/update-estimate.md) | `PUT /estimates/:id` | [docs](https://www.clientary.com/api/estimates) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://www.clientary.com/api/invoices) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://www.clientary.com/api/projects) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://www.clientary.com/api/tasks) |
