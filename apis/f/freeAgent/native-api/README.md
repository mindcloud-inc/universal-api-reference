# FreeAgent: Native API Reference

A consolidated summary of FreeAgent's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://dev.freeagent.com/docs
- **API base URL:** `https://api.freeagent.com/v2`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.freeagent.com/v2/approve_app to approve access.
2. Exchange the returned authorization code with a POST request to https://api.freeagent.com/v2/token_endpoint.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.freeagent.com/v2/token_endpoint.

[Official authentication documentation](https://dev.freeagent.com/docs/oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `contacts`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | `POST /bills` | [docs](https://dev.freeagent.com/docs/bills#create-a-bill) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://dev.freeagent.com/docs/contacts#create-a-contact) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://dev.freeagent.com/docs/estimates#create-an-estimate) |
| [Create Expense](actions/create-expense.md) | `POST /expenses` | [docs](https://dev.freeagent.com/docs/expenses#create-an-expense) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://dev.freeagent.com/docs/invoices#create-an-invoice) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://dev.freeagent.com/docs/projects#create-a-project) |
| [Get Bill](actions/get-bill.md) | `GET /bills/:id` | [docs](https://dev.freeagent.com/docs/bills#get-a-single-bill) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://dev.freeagent.com/docs/contacts#get-a-single-contact) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:id` | [docs](https://dev.freeagent.com/docs/estimates#get-a-single-estimate) |
| [Get Expense](actions/get-expense.md) | `GET /expenses/:id` | [docs](https://dev.freeagent.com/docs/expenses#get-a-single-expense) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://dev.freeagent.com/docs/invoices#get-a-single-invoice) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://dev.freeagent.com/docs/projects#get-a-single-project) |
| [List Bills](actions/list-bills.md) | `GET /bills` | [docs](https://dev.freeagent.com/docs/bills#list-all-bills) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://dev.freeagent.com/docs/contacts#list-all-contacts) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://dev.freeagent.com/docs/estimates#list-all-estimates) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://dev.freeagent.com/docs/expenses#list-all-expenses) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://dev.freeagent.com/docs/invoices#list-all-invoices) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://dev.freeagent.com/docs/projects#list-all-projects) |
| [Update Bill](actions/update-bill.md) | `PUT /bills/:id` | [docs](https://dev.freeagent.com/docs/bills#update-a-bill) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://dev.freeagent.com/docs/contacts#update-a-contact) |
| [Update Estimate](actions/update-estimate.md) | `PUT /estimates/:id` | [docs](https://dev.freeagent.com/docs/estimates#update-an-estimate) |
| [Update Expense](actions/update-expense.md) | `PUT /expenses/:id` | [docs](https://dev.freeagent.com/docs/expenses#update-an-expense) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://dev.freeagent.com/docs/invoices#update-an-invoice) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://dev.freeagent.com/docs/projects#update-a-project) |
