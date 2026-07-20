# Clockodo: Native API Reference

A consolidated summary of Clockodo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.clockodo.com/en/api/
- **OpenAPI specification:** https://docs.clockodo.com/openapi.yaml
- **API base URL:** `https://my.clockodo.com/api/v2`

## Authentication

### Clockodo API Key

Connect with the Clockodo API user email and API key.

### Credentials

- **API Key:** `apiKey` · required
- **API User Email:** `apiUserEmail` · required · Email address associated with the Clockodo API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.clockodo.com/en/api/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Accept-Language` | `en` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

The page size is configurable. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Duration](actions/change-duration.md) | `PUT /clock/:id` | [docs](https://www.clockodo.com/en/api/clock/) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://www.clockodo.com/en/api/customers/) |
| [Create Entry](actions/create-entry.md) | `POST /entries` | [docs](https://www.clockodo.com/en/api/entries/) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://www.clockodo.com/en/api/projects/) |
| [Create Service](actions/create-service.md) | `POST /services` | [docs](https://www.clockodo.com/en/api/services/) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://www.clockodo.com/en/api/customers/) |
| [Delete Entry](actions/delete-entry.md) | `DELETE /entries/:id` | [docs](https://www.clockodo.com/en/api/entries/) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://www.clockodo.com/en/api/projects/) |
| [Delete Service](actions/delete-service.md) | `DELETE /services/:id` | [docs](https://www.clockodo.com/en/api/services/) |
| [Get Currently Running Entries](actions/get-currently-running-entries.md) | `GET /clock` | [docs](https://www.clockodo.com/en/api/clock/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://www.clockodo.com/en/api/customers/) |
| [Get Entry](actions/get-entry.md) | `GET /entries/:id` | [docs](https://www.clockodo.com/en/api/entries/) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://www.clockodo.com/en/api/projects/) |
| [Get Service](actions/get-service.md) | `GET /services/:id` | [docs](https://www.clockodo.com/en/api/services/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.clockodo.com/en/api/customers/) |
| [List Entries](actions/list-entries.md) | `GET /entries` | [docs](https://www.clockodo.com/en/api/entries/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.clockodo.com/en/api/projects/) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://www.clockodo.com/en/api/services/) |
| [Start Clock](actions/start-clock.md) | `POST /clock` | [docs](https://www.clockodo.com/en/api/clock/) |
| [Stop Clock](actions/stop-clock.md) | `DELETE /clock/:id` | [docs](https://www.clockodo.com/en/api/clock/) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://www.clockodo.com/en/api/customers/) |
| [Update Entry](actions/update-entry.md) | `PUT /entries/:id` | [docs](https://www.clockodo.com/en/api/entries/) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://www.clockodo.com/en/api/projects/) |
| [Update Service](actions/update-service.md) | `PUT /services/:id` | [docs](https://www.clockodo.com/en/api/services/) |
