# Jitbit Helpdesk: Native API Reference

A consolidated summary of Jitbit Helpdesk's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.jitbit.com/docs/api/
- **API base URL:** `{helpdeskBaseUrl}/api`

## Authentication

### Bearer token

Connect Jitbit Helpdesk with a user token and your helpdesk base URL.

### Credentials

- **API Key:** `apiKey` · required
- **Helpdesk Base URL:** `helpdeskBaseUrl` · required · Your Jitbit Helpdesk base URL without the /api suffix, for example https://company.jitbit.com/helpdesk. This value is stored on the connection and used to build API requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.jitbit.com/docs/api/)

## Pagination

Use `count` in the query string to set the page size (default 50; accepted range 1–300). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | `GET /attachment` | [docs](https://www.jitbit.com/docs/api/#attachment) |
| [Get Parent Ticket](actions/get-parent-ticket.md) | `GET /ParentTicket` | [docs](https://www.jitbit.com/docs/api/#parent-ticket) |
| [Get Stats](actions/get-stats.md) | `GET /Stats` | [docs](https://www.jitbit.com/docs/api/#stats) |
| [Get Ticket](actions/get-ticket.md) | `GET /ticket` | [docs](https://www.jitbit.com/docs/api/#ticket) |
| [Get Ticket Integration Data](actions/get-ticket-integration-data.md) | `GET /TicketIntegrationData` | [docs](https://www.jitbit.com/docs/api/#ticket-integration-data) |
| [Get User](actions/get-user.md) | `GET /User` | [docs](https://www.jitbit.com/docs/api/#user-get) |
| [List Attachments](actions/list-attachments.md) | `GET /Attachments` | [docs](https://www.jitbit.com/docs/api/#attachments) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://www.jitbit.com/docs/api/#categories) |
| [List Comment Templates](actions/list-comment-templates.md) | `GET /CommentTemplates` | [docs](https://www.jitbit.com/docs/api/#comment-templates) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://www.jitbit.com/docs/api/#comments-2) |
| [List Custom Fields for Category](actions/list-custom-fields-for-category.md) | `GET /CustomFieldsForCategory` | [docs](https://www.jitbit.com/docs/api/#custom-fields-for-category) |
| [List Linked Tickets](actions/list-linked-tickets.md) | `GET /LinkedTickets` | [docs](https://www.jitbit.com/docs/api/#linked-tickets) |
| [List Priorities](actions/list-priorities.md) | `GET /Priorities` | [docs](https://www.jitbit.com/docs/api/#priorities-get) |
| [List Subscribers](actions/list-subscribers.md) | `GET /Subscribers` | [docs](https://www.jitbit.com/docs/api/#subscribers-get) |
| [List Subtickets](actions/list-subtickets.md) | `GET /SubTickets` | [docs](https://www.jitbit.com/docs/api/#sub-tickets) |
| [List Techs for Category](actions/list-techs-for-category.md) | `GET /TechsForCategory` | [docs](https://www.jitbit.com/docs/api/#techs-for-category) |
| [List Ticket Custom Fields](actions/list-ticket-custom-fields.md) | `GET /TicketCustomFields` | [docs](https://www.jitbit.com/docs/api/#ticket-custom-fields) |
| [List Tickets](actions/list-tickets.md) | `GET /Tickets` | [docs](https://www.jitbit.com/docs/api/#tickets) |
| [List Time Spent Log](actions/list-time-spent-log.md) | `GET /TimeSpentLog` | [docs](https://www.jitbit.com/docs/api/#time-spent-log-get) |
| [Search Tickets](actions/search-tickets.md) | `GET /Search` | [docs](https://www.jitbit.com/docs/api/#search) |
