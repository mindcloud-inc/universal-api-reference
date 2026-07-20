# Simplicate: Native API Reference

A consolidated summary of Simplicate's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://developer.simplicate.com/docs/api/v2/getting_started/
- **OpenAPI specification:** https://swagger.simplicate.app/openapi.yaml
- **API base URL:** `https://{subdomain}/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · The company part of your Simplicate URL, for example `mindcloud`.
- **API Secret:** `apiSecret` · required · The API secret shown when the Simplicate token is created.

Send these headers with each API request:

```http
Authentication-Key: <apiKey>
Authentication-Secret: <apiSecret>
```

[Official authentication documentation](https://developer.simplicate.com/docs/api/v2/getting_started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | `POST /hrm/employee` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-hrm-employee/) |
| [Create Hour Entry](actions/create-hour-entry.md) | `POST /hours/hours` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-hours-hours/) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices/invoice` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-invoices-invoice/) |
| [Create Organization](actions/create-organization.md) | `POST /crm/organization` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-crm-organization/) |
| [Create Payment](actions/create-payment.md) | `POST /invoices/payment` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-invoices-payment/) |
| [Create Person](actions/create-person.md) | `POST /crm/person` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-crm-person/) |
| [Create Project](actions/create-project.md) | `POST /projects/project` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-projects-project/) |
| [Create Quote Template](actions/create-quote-template.md) | `POST /sales/quote` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-sales-quote/) |
| [Create Sale](actions/create-sale.md) | `POST /sales/sales` | [docs](https://developer.simplicate.com/docs/api/v2/reference/create-sales-sales/) |
| [Get Employee](actions/get-employee.md) | `GET /hrm/employee/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-hrm-employee-by-id/) |
| [Get Hour Entry](actions/get-hour-entry.md) | `GET /hours/hours/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-hours-hours-by-id/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/invoice/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-invoices-invoice-by-id/) |
| [Get Organization](actions/get-organization.md) | `GET /crm/organization/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-crm-organization-by-id/) |
| [Get Person](actions/get-person.md) | `GET /crm/person/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-crm-person-by-id/) |
| [Get Project](actions/get-project.md) | `GET /projects/project/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-projects-project-by-id/) |
| [Get Quote Template](actions/get-quote-template.md) | `GET /sales/quote/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-sales-quote-by-id/) |
| [Get Sale](actions/get-sale.md) | `GET /sales/sales/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-sales-sales-by-id/) |
| [Get Service](actions/get-service.md) | `GET /projects/service/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-projects-service-by-id/) |
| [List Employees](actions/list-employees.md) | `GET /hrm/employee` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-hrm-employee/) |
| [List Hours](actions/list-hours.md) | `GET /hours/hours` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-hours-hours/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices/invoice` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-invoices-invoice/) |
| [List Organizations](actions/list-organizations.md) | `GET /crm/organization` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-crm-organization/) |
| [List Payments](actions/list-payments.md) | `GET /invoices/payment` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-invoices-payment/) |
| [List Persons](actions/list-persons.md) | `GET /crm/person` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-crm-person/) |
| [List Projects](actions/list-projects.md) | `GET /projects/project` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-projects-project/) |
| [List Quote Templates](actions/list-quote-templates.md) | `GET /sales/quote` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-sales-quote/) |
| [List Sales](actions/list-sales.md) | `GET /sales/sales` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-sales-sales/) |
| [List Services](actions/list-services.md) | `GET /projects/service` | [docs](https://developer.simplicate.com/docs/api/v2/reference/get-projects-service/) |
| [Update Employee](actions/update-employee.md) | `PUT /hrm/employee/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-hrm-employee/) |
| [Update Hour Entry](actions/update-hour-entry.md) | `PUT /hours/hours/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-hours-hours/) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/invoice/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-invoices-invoice/) |
| [Update Organization](actions/update-organization.md) | `PUT /crm/organization/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-crm-organization/) |
| [Update Person](actions/update-person.md) | `PUT /crm/person/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-crm-person/) |
| [Update Project](actions/update-project.md) | `PUT /projects/project/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-projects-project/) |
| [Update Quote Template](actions/update-quote-template.md) | `PUT /sales/quote/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-sales-quote/) |
| [Update Sale](actions/update-sale.md) | `PUT /sales/sales/:id` | [docs](https://developer.simplicate.com/docs/api/v2/reference/update-sales-sales/) |
