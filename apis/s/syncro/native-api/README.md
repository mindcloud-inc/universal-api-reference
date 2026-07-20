# Syncro: Native API Reference

A consolidated summary of Syncro's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.syncromsp.com/
- **OpenAPI specification:** https://api-docs.syncromsp.com/swagger.json
- **API base URL:** `https://mindcloud.syncromsp.com/api/v1`

## Authentication

### API Key

Authenticate to Syncro with an API key sent in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.syncromsp.com/en_US/third-party-integrations/syncro-api)

## API conventions

Responses from this API use JSON. Response data is read from `customers`. The total page count is read from `meta.total_pages`. The current page number is read from `meta.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Ticket Comment](actions/add-ticket-comment.md) | `POST /tickets/:id/comment` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [Add Ticket Line Item](actions/add-ticket-line-item.md) | `POST /tickets/:id/add_line_item` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [Convert Estimate To Invoice](actions/convert-estimate-to-invoice.md) | `POST /estimates/:id/convert_to_invoice` | [docs](https://api-docs.syncromsp.com/#/Estimate/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api-docs.syncromsp.com/#/Contact/) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://api-docs.syncromsp.com/#/Customer/) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://api-docs.syncromsp.com/#/Estimate/) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://api-docs.syncromsp.com/#/Invoice/) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [Create Ticket Timer](actions/create-ticket-timer.md) | `POST /tickets/:id/timer_entry` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api-docs.syncromsp.com/#/Contact/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://api-docs.syncromsp.com/#/Customer/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://api-docs.syncromsp.com/#/Invoice/) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:id` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [List Assets](actions/list-assets.md) | `GET /customer_assets` | [docs](https://api-docs.syncromsp.com/#/Asset/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api-docs.syncromsp.com/#/Contact/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api-docs.syncromsp.com/#/Customer/) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://api-docs.syncromsp.com/#/Estimate/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://api-docs.syncromsp.com/#/Invoice/) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://api-docs.syncromsp.com/#/Payment/) |
| [List Ticket Comments](actions/list-ticket-comments.md) | `GET /tickets/:id/comments` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://api-docs.syncromsp.com/#/Contact/) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://api-docs.syncromsp.com/#/Customer/) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://api-docs.syncromsp.com/#/Invoice/) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:id` | [docs](https://api-docs.syncromsp.com/#/Ticket/) |
