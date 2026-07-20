# GrooveHQ: Native API Reference

A consolidated summary of GrooveHQ's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://doc.groovehq.com/
- **API base URL:** `https://api.groovehq.com/v1`

## Authentication

### API Key

Use a Groove private access token from the account API settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.groovehq.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Ticket Labels](actions/add-ticket-labels.md) | `POST /tickets/:ticketNumber/tags` | [docs](https://doc.groovehq.com/tickets) |
| [Change Ticket Mailbox](actions/change-ticket-mailbox.md) | `POST /tickets/:ticketId/change_mailbox/:mailboxId` | [docs](https://doc.groovehq.com/tickets) |
| [Create Message](actions/create-message.md) | `POST /tickets/:ticketNumber/messages` | [docs](https://doc.groovehq.com/messages) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://doc.groovehq.com/tickets) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentEmail` | [docs](https://doc.groovehq.com/agents) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://doc.groovehq.com/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerEmail` | [docs](https://doc.groovehq.com/customers) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /kb/:id` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://doc.groovehq.com/messages) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:ticketNumber` | [docs](https://doc.groovehq.com/tickets) |
| [Get Ticket Assignee](actions/get-ticket-assignee.md) | `GET /tickets/:ticketNumber/assignee` | [docs](https://doc.groovehq.com/tickets) |
| [Get Ticket State](actions/get-ticket-state.md) | `GET /tickets/:ticketNumber/state` | [docs](https://doc.groovehq.com/tickets) |
| [Get Widget](actions/get-widget.md) | `GET /public/widgets/:widgetUuid` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://doc.groovehq.com/agents) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://doc.groovehq.com/customers) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://doc.groovehq.com/folders) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://doc.groovehq.com/groups) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /kb` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /mailboxes` | [docs](https://doc.groovehq.com/mailboxes) |
| [List Messages](actions/list-messages.md) | `GET /tickets/:ticketNumber/messages` | [docs](https://doc.groovehq.com/messages) |
| [List Ticket Counts](actions/list-ticket-counts.md) | `GET /tickets/count` | [docs](https://doc.groovehq.com/ticket-counts) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://doc.groovehq.com/tickets) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [Replace Ticket Labels](actions/replace-ticket-labels.md) | `PUT /tickets/:ticketNumber/tags` | [docs](https://doc.groovehq.com/tickets) |
| [Search Knowledge Base Articles](actions/search-kb-articles.md) | `GET /kb/public/:knowledgeBaseId/articles/search` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [Search Knowledge Base Categories](actions/search-kb-categories.md) | `GET /kb/:knowledgeBaseId/categories/search` | [docs](https://doc.groovehq.com/knowledge-bases) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customerEmail` | [docs](https://doc.groovehq.com/customers) |
| [Update Ticket Assignee](actions/update-ticket-assignee.md) | `PUT /tickets/:ticketNumber/assignee` | [docs](https://doc.groovehq.com/tickets) |
| [Update Ticket Group](actions/update-ticket-group.md) | `PUT /tickets/:ticketNumber/assigned_group` | [docs](https://doc.groovehq.com/tickets) |
| [Update Ticket State](actions/update-ticket-state.md) | `PUT /tickets/:ticketNumber/state` | [docs](https://doc.groovehq.com/tickets) |
