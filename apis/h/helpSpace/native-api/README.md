# HelpSpace: Native API Reference

A consolidated summary of HelpSpace's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://documentation.helpspace.com
- **API base URL:** `https://api.helpspace.com/api/v1`

## Authentication

### API Key

Authenticate HelpSpace with the implicit bearer API key plus a required Hs-Client-Id header for the workspace.

### Credentials

- **API Key:** `apiKey` · required
- **Client ID:** `hsClientId` · required · HelpSpace workspace client identifier required for the Hs-Client-Id header on every API request.

Send these headers with each API request:

```http
Hs-Client-Id: <hsClientId>
```

[Official authentication documentation](https://documentation.helpspace.com/api-access-tokens-and-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `per-page` in the query string to set the page size (accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://documentation.helpspace.com/api-customers) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://documentation.helpspace.com/api-tags) |
| [Create Task](actions/create-task.md) | `POST /scrum/tasks` | [docs](https://documentation.helpspace.com/api-tasks) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://documentation.helpspace.com/api-tickets) |
| [Create Ticket Message](actions/create-ticket-message.md) | `POST /tickets/{id}/messages` | [docs](https://documentation.helpspace.com/api-message) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/{id}` | [docs](https://documentation.helpspace.com/api-customers) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/{id}` | [docs](https://documentation.helpspace.com/api-tags) |
| [Delete Task](actions/delete-task.md) | `DELETE /scrum/tasks/{id}` | [docs](https://documentation.helpspace.com/api-tasks) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/{id}` | [docs](https://documentation.helpspace.com/api-tickets) |
| [Get Attachment Media](actions/get-attachment-media.md) | `GET /media/attachment/{id}` | [docs](https://documentation.helpspace.com/api-message) |
| [Get Channels Report](actions/get-channels-report.md) | `POST /reports/channels` | [docs](https://documentation.helpspace.com/api-reports) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{id}` | [docs](https://documentation.helpspace.com/api-customers) |
| [Get Customer Avatar](actions/get-customer-avatar.md) | `GET /customers/{id}/avatar` | [docs](https://documentation.helpspace.com/api-customers) |
| [Get Docs Article](actions/get-docs-article.md) | `GET /docs/articles/{id}` | [docs](https://documentation.helpspace.com/api-docs-articles) |
| [Get Inline Media](actions/get-inline-media.md) | `GET /media/inline/{id}/{size}` | [docs](https://documentation.helpspace.com/api-message) |
| [Get Performance Report](actions/get-performance-report.md) | `POST /reports/performance` | [docs](https://documentation.helpspace.com/api-reports) |
| [Get Tag](actions/get-tag.md) | `GET /tags/{id}` | [docs](https://documentation.helpspace.com/api-tags) |
| [Get Task](actions/get-task.md) | `GET /scrum/tasks/{id}` | [docs](https://documentation.helpspace.com/api-tasks) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/{id}` | [docs](https://documentation.helpspace.com/api-tickets) |
| [Get Ticket Message](actions/get-ticket-message.md) | `GET /tickets/{ticket_id}/messages/{message_id}` | [docs](https://documentation.helpspace.com/api-message) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook` | [docs](https://documentation.helpspace.com/article/340/webhook) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://documentation.helpspace.com/api-customers) |
| [List Docs Articles](actions/list-docs-articles.md) | `GET /docs/articles` | [docs](https://documentation.helpspace.com/api-docs-articles) |
| [List Docs Categories](actions/list-docs-categories.md) | `GET /docs/categories` | [docs](https://documentation.helpspace.com/api-docs-categories) |
| [List Docs Sites](actions/list-docs-sites.md) | `GET /docs/sites` | [docs](https://documentation.helpspace.com/api-docs-sites) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://documentation.helpspace.com/api-tags) |
| [List Tasks](actions/list-tasks.md) | `GET /scrum/tasks` | [docs](https://documentation.helpspace.com/api-tasks) |
| [List Ticket Messages](actions/list-ticket-messages.md) | `GET /tickets/{id}/messages` | [docs](https://documentation.helpspace.com/api-message) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://documentation.helpspace.com/api-tickets) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `GET /webhook/logs` | [docs](https://documentation.helpspace.com/article/340/webhook) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/{id}` | [docs](https://documentation.helpspace.com/api-customers) |
| [Update Customer Avatar](actions/update-customer-avatar.md) | `PATCH /customers/{id}/avatar` | [docs](https://documentation.helpspace.com/api-customers) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/{id}` | [docs](https://documentation.helpspace.com/api-tags) |
| [Update Task](actions/update-task.md) | `PATCH /scrum/tasks/{id}` | [docs](https://documentation.helpspace.com/api-tasks) |
| [Update Ticket](actions/update-ticket.md) | `PATCH /tickets/{id}` | [docs](https://documentation.helpspace.com/api-tickets) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhook` | [docs](https://documentation.helpspace.com/article/340/webhook) |
