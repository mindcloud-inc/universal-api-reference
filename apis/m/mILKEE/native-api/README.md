# MILKEE: Native API Reference

A consolidated summary of MILKEE's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.milkee.ch/api/
- **API base URL:** `https://app.milkee.ch/api/v2`

## Authentication

### Personal Access Token

Use a MILKEE personal access token. Requests send the token as a Bearer value in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.milkee.ch/api/authentifizierung.html)

## API conventions

Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /companies/:companyId/customers` | [docs](https://apidocs.milkee.ch/api/resources/customers.html#neuen-customer-erstellen) |
| [Create Invoice](actions/create-invoice.md) | `POST /companies/:companyId/invoices` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#neue-rechnung-erstellen) |
| [Create Project](actions/create-project.md) | `POST /companies/:companyId/projects` | [docs](https://apidocs.milkee.ch/api/resources/projects.html#neues-project-erstellen) |
| [Create Proposal](actions/create-proposal.md) | `POST /companies/:companyId/proposals` | [docs](https://apidocs.milkee.ch/api/resources/proposals.html#neue-offerte-erstellen) |
| [Create Task](actions/create-task.md) | `POST /companies/:companyId/tasks` | [docs](https://apidocs.milkee.ch/api/resources/tasks.html#create-a-task) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /companies/:companyId/times` | [docs](https://apidocs.milkee.ch/api/resources/times.html#create-a-time-entry) |
| [Get Customer](actions/get-customer.md) | `GET /companies/:companyId/customers/:customerId` | [docs](https://apidocs.milkee.ch/api/resources/customers.html#einzelnen-customer-abrufen) |
| [Get Customer Statistics](actions/get-customer-statistics.md) | `GET /companies/:companyId/customers/:customerId/statistics` | [docs](https://apidocs.milkee.ch/api/resources/customers.html#kundenstatistiken-abrufen) |
| [Get Invoice](actions/get-invoice.md) | `GET /companies/:companyId/invoices/:invoiceId` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#einzelne-rechnung-abrufen) |
| [Get Next Invoice Number](actions/get-next-invoice-number.md) | `GET /companies/:companyId/invoices/number` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#nachste-rechnungsnummer-abrufen) |
| [Get Project](actions/get-project.md) | `GET /companies/:companyId/projects/:projectId` | [docs](https://apidocs.milkee.ch/api/resources/projects.html#einzelnes-project-abrufen) |
| [Get Proposal](actions/get-proposal.md) | `GET /companies/:companyId/proposals/:proposalId` | [docs](https://apidocs.milkee.ch/api/resources/proposals.html#einzelne-offerte-abrufen) |
| [Get Task](actions/get-task.md) | `GET /companies/:companyId/tasks/:taskId` | [docs](https://apidocs.milkee.ch/api/resources/tasks.html#retrieve-a-task) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /companies/:companyId/times/:timeId` | [docs](https://apidocs.milkee.ch/api/resources/times.html#retrieve-a-time-entry) |
| [Get Timer Status](actions/get-timer-status.md) | `GET /companies/:companyId/times/timer` | [docs](https://apidocs.milkee.ch/api/resources/times.html#get-timer-status) |
| [List Customers](actions/list-customers.md) | `GET /companies/:companyId/customers` | [docs](https://apidocs.milkee.ch/api/resources/customers.html#alle-customers-auflisten) |
| [List Invoices](actions/list-invoices.md) | `GET /companies/:companyId/invoices` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#alle-rechnungen-auflisten) |
| [List Projects](actions/list-projects.md) | `GET /companies/:companyId/projects` | [docs](https://apidocs.milkee.ch/api/resources/projects.html#alle-projects-auflisten) |
| [List Proposals](actions/list-proposals.md) | `GET /companies/:companyId/proposals` | [docs](https://apidocs.milkee.ch/api/resources/proposals.html#alle-offerten-auflisten) |
| [List Tasks](actions/list-tasks.md) | `GET /companies/:companyId/tasks` | [docs](https://apidocs.milkee.ch/api/resources/tasks.html#list-all-tasks) |
| [List Time Entries](actions/list-time-entries.md) | `GET /companies/:companyId/times` | [docs](https://apidocs.milkee.ch/api/resources/times.html#list-time-entries) |
| [Start Or Stop Timer](actions/start-or-stop-timer.md) | `POST /companies/:companyId/times/timer` | [docs](https://apidocs.milkee.ch/api/resources/times.html#start-stop-timer) |
| [Update Customer](actions/update-customer.md) | `PUT /companies/:companyId/customers/:customerId` | [docs](https://apidocs.milkee.ch/api/resources/customers.html#customer-aktualisieren) |
| [Update Invoice](actions/update-invoice.md) | `PUT /companies/:companyId/invoices/:invoiceId` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#rechnung-aktualisieren) |
| [Update Invoice Status](actions/update-invoice-status.md) | `GET /companies/:companyId/invoices/:invoiceId/mark-as` | [docs](https://apidocs.milkee.ch/api/resources/invoices.html#status-andern-mark-as) |
| [Update Project](actions/update-project.md) | `PUT /companies/:companyId/projects/:projectId` | [docs](https://apidocs.milkee.ch/api/resources/projects.html#project-aktualisieren) |
| [Update Proposal](actions/update-proposal.md) | `PUT /companies/:companyId/proposals/:proposalId` | [docs](https://apidocs.milkee.ch/api/resources/proposals.html#offerte-aktualisieren) |
| [Update Proposal Status](actions/update-proposal-status.md) | `GET /companies/:companyId/proposals/:proposalId/mark-as` | [docs](https://apidocs.milkee.ch/api/resources/proposals.html#status-andern-mark-as) |
| [Update Task](actions/update-task.md) | `PUT /companies/:companyId/tasks/:taskId` | [docs](https://apidocs.milkee.ch/api/resources/tasks.html#update-a-task) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /companies/:companyId/times/:timeId` | [docs](https://apidocs.milkee.ch/api/resources/times.html#update-a-time-entry) |
