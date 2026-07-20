# Mendato: Native API Reference

A consolidated summary of Mendato's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.mendato.com
- **API base URL:** `https://api.mendato.com`

## Authentication

### API Key

Authenticate Mendato with a company-bound API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.mendato.com/de/articles/14093248-api-keys)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /graphql` | [docs](https://developers.mendato.com/#mutation-createCustomer) |
| [Create Estimate](actions/create-estimate.md) | `POST /graphql` | [docs](https://developers.mendato.com/#mutation-createEstimate) |
| [Create Invoice](actions/create-invoice.md) | `POST /graphql` | [docs](https://developers.mendato.com/#mutation-createInvoice) |
| [Get Company](actions/get-company.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-company) |
| [Get Customer](actions/get-customer.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-customer) |
| [Get Employee](actions/get-employee.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-employee) |
| [Get Estimate](actions/get-estimate.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-estimate) |
| [Get Invoice](actions/get-invoice.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-invoice) |
| [Get Next Employee Personnel Number](actions/get-next-employee-personnel-number.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-nextEmployeePersonnelNumber) |
| [Get Object](actions/get-object.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-object) |
| [Get Operation](actions/get-operation.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-operation) |
| [Get Order](actions/get-order.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-order) |
| [Get Ticket](actions/get-ticket.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-ticket) |
| [List Customers](actions/list-customers.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-customers) |
| [List Employees](actions/list-employees.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-employees) |
| [List Estimates](actions/list-estimates.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-estimates) |
| [List Invoices](actions/list-invoices.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-invoices) |
| [List Objects](actions/list-objects.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-objects) |
| [List Operations](actions/list-operations.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-operations) |
| [List Orders](actions/list-orders.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-orders) |
| [List Tickets](actions/list-tickets.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-tickets) |
| [List Time Records](actions/list-time-records.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-timeRecords) |
| [List Unassigned Operations](actions/list-unassigned-operations.md) | `POST /graphql` | [docs](https://developers.mendato.com/#query-unassignedOperations) |
| [Update Customer](actions/update-customer.md) | `POST /graphql` | [docs](https://developers.mendato.com/#mutation-updateCustomer) |
