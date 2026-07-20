# Atera: Native API Reference

A consolidated summary of Atera's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.atera.com/apidocs
- **OpenAPI specification:** https://app.atera.com/swagger/docs/v3
- **API base URL:** `https://app.atera.com`

## Authentication

### API Key

Connect with an Atera API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.atera.com/hc/en-us/articles/219083397-APIs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `itemsInPage` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add ticket comment](actions/add-ticket-comment.md) | `POST /api/v3/tickets/:ticketId/comments` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_AddCommentToTicketAsync) |
| [Create alert](actions/create-alert.md) | `POST /api/v3/alerts` | [docs](https://app.atera.com/apidocs#!/Alert/Alert_Post) |
| [Create contact](actions/create-contact.md) | `POST /api/v3/contacts` | [docs](https://app.atera.com/apidocs#!/Contact/Contact_Post) |
| [Create customer](actions/create-customer.md) | `POST /api/v3/customers` | [docs](https://app.atera.com/apidocs#!/Customer/Customer_Post) |
| [Create ticket](actions/create-ticket.md) | `POST /api/v3/tickets` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_Post) |
| [Find agents](actions/find-agents.md) | `GET /api/v3/agents` | [docs](https://app.atera.com/apidocs#!/Agent/Agent_Get) |
| [Find agents for customer](actions/find-agents-for-customer.md) | `GET /api/v3/agents/customer/:customerId` | [docs](https://app.atera.com/apidocs#!/Agent/Agent_GetByCustomer) |
| [Find alerts](actions/find-alerts.md) | `GET /api/v3/alerts` | [docs](https://app.atera.com/apidocs) |
| [Find contacts](actions/find-contacts.md) | `GET /api/v3/contacts` | [docs](https://app.atera.com/apidocs) |
| [Find customers](actions/find-customers.md) | `GET /api/v3/customers` | [docs](https://app.atera.com/apidocs) |
| [Find modified tickets](actions/find-modified-tickets.md) | `GET /api/v3/tickets/lastmodified` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_GetTicketsByLastModifiedAsync) |
| [Find ticket attachments](actions/find-ticket-attachments.md) | `GET /api/v3/tickets/:ticketId/attachments` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_GetAttachmentsByTicketIdAsync) |
| [Find ticket comments](actions/find-ticket-comments.md) | `GET /api/v3/tickets/:ticketId/comments` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_GetComments) |
| [Find tickets](actions/find-tickets.md) | `GET /api/v3/tickets` | [docs](https://app.atera.com/apidocs) |
| [Get account info](actions/get-account-info.md) | `GET /api/v3/account` | [docs](https://app.atera.com/apidocs#!/Account/Account_GetAccountInfo) |
| [Get agent](actions/get-agent.md) | `GET /api/v3/agents/:agentId` | [docs](https://app.atera.com/apidocs#!/Agent/Agent_AgentQueryDTO) |
| [Get alert](actions/get-alert.md) | `GET /api/v3/alerts/:alertId` | [docs](https://app.atera.com/apidocs) |
| [Get contact](actions/get-contact.md) | `GET /api/v3/contacts/:contactId` | [docs](https://app.atera.com/apidocs) |
| [Get customer](actions/get-customer.md) | `GET /api/v3/customers/:customerId` | [docs](https://app.atera.com/apidocs) |
| [Get ticket](actions/get-ticket.md) | `GET /api/v3/tickets/:ticketId` | [docs](https://app.atera.com/apidocs) |
| [Resolve alert](actions/resolve-alert.md) | `PUT /api/v3/alerts/:alertId` | [docs](https://app.atera.com/apidocs#!/Alert/Alert_ResolveAlert) |
| [Update contact](actions/update-contact.md) | `PUT /api/v3/contacts/:contactId` | [docs](https://app.atera.com/apidocs#!/Contact/Contact_Put) |
| [Update customer](actions/update-customer.md) | `PUT /api/v3/customers/:customerId` | [docs](https://app.atera.com/apidocs#!/Customer/Customer_Put) |
| [Update ticket](actions/update-ticket.md) | `PUT /api/v3/tickets/:ticketId` | [docs](https://app.atera.com/apidocs#!/Ticket/Ticket_Put) |
