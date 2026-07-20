# FreshBooks: Native API Reference

A consolidated summary of FreshBooks's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.freshbooks.com/api/start
- **API base URL:** `https://api.freshbooks.com`

## Authentication

### OAuth2

OAuth2 authorization code flow for FreshBooks APIs.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.freshbooks.com/oauth/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://api.freshbooks.com/auth/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user:profile:read user:clients:read user:clients:write user:invoices:read user:invoices:write user:estimates:read user:estimates:write user:expenses:read user:expenses:write user:projects:read user:projects:write user:time_entries:read user:time_entries:write user:billable_items:read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.freshbooks.com/auth/oauth/token.

[Official authentication documentation](https://www.freshbooks.com/api/authentication)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /accounting/account/:accountId/users/clients` | [docs](https://www.freshbooks.com/api/clients) |
| [Create Estimate](actions/create-estimate.md) | `POST /accounting/account/:accountId/estimates/estimates` | [docs](https://www.freshbooks.com/api/estimates) |
| [Create Expense](actions/create-expense.md) | `POST /accounting/account/:accountId/expenses/expenses` | [docs](https://www.freshbooks.com/api/expenses) |
| [Create Invoice](actions/create-invoice.md) | `POST /accounting/account/:accountId/invoices/invoices` | [docs](https://www.freshbooks.com/api/invoices) |
| [Create Project](actions/create-project.md) | `POST /projects/business/:businessId/project` | [docs](https://www.freshbooks.com/api/project) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /timetracking/business/:businessId/time_entries` | [docs](https://www.freshbooks.com/api/time_entries) |
| [Get Client](actions/get-client.md) | `GET /accounting/account/:accountId/users/clients/:userId` | [docs](https://www.freshbooks.com/api/clients) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /auth/api/v1/users/me` | [docs](https://www.freshbooks.com/api/identity_model) |
| [Get Estimate](actions/get-estimate.md) | `GET /accounting/account/:accountId/estimates/estimates/:estimateId` | [docs](https://www.freshbooks.com/api/estimates) |
| [Get Expense](actions/get-expense.md) | `GET /accounting/account/:accountId/expenses/expenses/:expenseId` | [docs](https://www.freshbooks.com/api/expenses) |
| [Get Invoice](actions/get-invoice.md) | `GET /accounting/account/:accountId/invoices/invoices/:invoiceId` | [docs](https://www.freshbooks.com/api/invoices) |
| [Get Project](actions/get-project.md) | `GET /projects/business/:businessId/project/:projectId` | [docs](https://www.freshbooks.com/api/project) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /timetracking/business/:businessId/time_entries/:timeEntryId` | [docs](https://www.freshbooks.com/api/time_entries) |
| [List Clients](actions/list-clients.md) | `GET /accounting/account/:accountId/users/clients` | [docs](https://www.freshbooks.com/api/clients) |
| [List Estimates](actions/list-estimates.md) | `GET /accounting/account/:accountId/estimates/estimates` | [docs](https://www.freshbooks.com/api/estimates) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET /accounting/account/:accountId/expenses/categories` | [docs](https://www.freshbooks.com/api/expenses) |
| [List Expenses](actions/list-expenses.md) | `GET /accounting/account/:accountId/expenses/expenses` | [docs](https://www.freshbooks.com/api/expenses) |
| [List Invoices](actions/list-invoices.md) | `GET /accounting/account/:accountId/invoices/invoices` | [docs](https://www.freshbooks.com/api/invoices) |
| [List Projects](actions/list-projects.md) | `GET /projects/business/:businessId/projects` | [docs](https://www.freshbooks.com/api/project) |
| [List Time Entries](actions/list-time-entries.md) | `GET /timetracking/business/:businessId/time_entries` | [docs](https://www.freshbooks.com/api/time_entries) |
| [Update Client](actions/update-client.md) | `PUT /accounting/account/:accountId/users/clients/:userId` | [docs](https://www.freshbooks.com/api/clients) |
| [Update Estimate](actions/update-estimate.md) | `PUT /accounting/account/:accountId/estimates/estimates/:estimateId` | [docs](https://www.freshbooks.com/api/estimates) |
| [Update Expense](actions/update-expense.md) | `PUT /accounting/account/:accountId/expenses/expenses/:expenseId` | [docs](https://www.freshbooks.com/api/expenses) |
| [Update Invoice](actions/update-invoice.md) | `PUT /accounting/account/:accountId/invoices/invoices/:invoiceId` | [docs](https://www.freshbooks.com/api/invoices) |
| [Update Project](actions/update-project.md) | `PUT /projects/business/:businessId/project/:projectId` | [docs](https://www.freshbooks.com/api/project) |
