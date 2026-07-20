# Assembly.com: Native API Reference

A consolidated summary of Assembly.com's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.assembly.com/reference
- **API base URL:** `https://api.assembly.com/v1`

## Authentication

### API Key

Use an Assembly API key sent in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.assembly.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `nextToken` in the query string as the pagination cursor.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /subscriptions/:id/cancel` | [docs](https://docs.assembly.com/reference/cancel-subscription) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://docs.assembly.com/reference/create-client) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://docs.assembly.com/reference/create-invoice) |
| [Create Message Channel](actions/create-message-channel.md) | `POST /message-channels` | [docs](https://docs.assembly.com/reference/create-message-channel) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://docs.assembly.com/reference/create-note) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://docs.assembly.com/reference/create-subscription) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://docs.assembly.com/reference/create-task) |
| [List App Installs](actions/list-app-installs.md) | `GET /installs` | [docs](https://docs.assembly.com/reference/list-app-installs) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://docs.assembly.com/reference/list-clients) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://docs.assembly.com/reference/list-companies) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://docs.assembly.com/reference/list-contracts) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.assembly.com/reference/list-invoices) |
| [List Message Channels](actions/list-message-channels.md) | `GET /message-channels` | [docs](https://docs.assembly.com/reference/list-message-channels) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://docs.assembly.com/reference/list-messages) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://docs.assembly.com/reference/list-notes) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://docs.assembly.com/reference/list-payments) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://docs.assembly.com/reference/list-subscriptions) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://docs.assembly.com/reference/retrieve-tasks) |
| [Retrieve Client](actions/retrieve-client.md) | `GET /clients/:id` | [docs](https://docs.assembly.com/reference/retrieve-client) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /companies/:id` | [docs](https://docs.assembly.com/reference/retrieve-company) |
| [Retrieve Contract](actions/retrieve-contract.md) | `GET /contracts/:id` | [docs](https://docs.assembly.com/reference/retrieve-contract) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /invoices/:id` | [docs](https://docs.assembly.com/reference/retrieve-invoice) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /tasks/:id` | [docs](https://docs.assembly.com/reference/retrieve-task) |
| [Send Contract](actions/send-contract.md) | `POST /contracts` | [docs](https://docs.assembly.com/reference/send-contract) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://docs.assembly.com/reference/send-message) |
| [Update Client](actions/update-client.md) | `PATCH /clients/:id` | [docs](https://docs.assembly.com/reference/update-client) |
| [Update Company](actions/update-company.md) | `PATCH /companies/:id` | [docs](https://docs.assembly.com/reference/update-company) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://docs.assembly.com/reference/update-task) |
