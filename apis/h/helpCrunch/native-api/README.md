# HelpCrunch: Native API Reference

A consolidated summary of HelpCrunch's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.helpcrunch.com/en/rest-api-v1
- **API base URL:** `https://api.helpcrunch.com/v1`

## Authentication

### API Key

Authenticate HelpCrunch REST API requests with your permanent API key using the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.helpcrunch.com/en/rest-api-v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer Event](actions/add-customer-event.md) | `POST /events` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/add-customer-event-v1) |
| [Batch Update Customers](actions/batch-update-customers.md) | `PUT /customers/batch` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/batch-update-customers-v1) |
| [Create Agent Message](actions/create-agent-message.md) | `POST /messages` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/create-message-v1) |
| [Create Chat](actions/create-chat.md) | `POST /chats` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/create-chat-v1) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/create-customer-v1) |
| [Create Customer Message](actions/create-customer-message.md) | `POST /messages` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/create-message-v1) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:customerId` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/delete-customer-v1) |
| [Get Chat](actions/get-chat.md) | `GET /chats/:chatId` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-chat-v1) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-customer-v1) |
| [Get Team Availability Status](actions/get-team-availability-status.md) | `GET /organization` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-organization-v1) |
| [List Applications](actions/list-applications.md) | `GET /applications` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-applications-v1) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chats/:chatId/messages` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-messages-v1) |
| [List Chats](actions/list-chats.md) | `GET /chats` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-chats-v1) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-customers-v1) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-departments-v1) |
| [List Team Members](actions/list-team-members.md) | `GET /agents` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/get-agents-v1) |
| [Mark Chat As Read By Agent](actions/mark-chat-as-read-by-agent.md) | `PUT /chats/readByAgent` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/read-chat-rest-api-1) |
| [Mark Chat As Read By Customer](actions/mark-chat-as-read-by-customer.md) | `PUT /chats/readByCustomer` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/read-chat-rest-api-1) |
| [Patch Customer](actions/patch-customer.md) | `PATCH /customers/:customerId` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/update-customer-v1) |
| [Rate Chat](actions/rate-chat.md) | `PUT /chats/rate` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/chat-rating-rest-api) |
| [Search Chats](actions/search-chats.md) | `POST /chats/search` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/search-chats-v1) |
| [Search Customers](actions/search-customers.md) | `POST /customers/search` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/search-customers-v1) |
| [Snooze Chat](actions/snooze-chat.md) | `PUT /chats/snooze` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/snooze-chat-v1) |
| [Tag Customer](actions/tag-customer.md) | `PUT /customers/:customerId/tags` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/tag-customer-v1) |
| [Unsubscribe Team Member](actions/unsubscribe-team-member.md) | `GET /agents/:agentId/unsubscribe` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/unsubscribe-agent-v1) |
| [Untag Customer](actions/untag-customer.md) | `DELETE /customers/:customerId/tags` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/untag-customer-v1) |
| [Update Chat Assignee](actions/update-chat-assignee.md) | `PUT /chats/assignee` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/update-chat-assignee-v1) |
| [Update Chat Department](actions/update-chat-department.md) | `PUT /chats/department` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/update-chat-department-v1) |
| [Update Chat Status](actions/update-chat-status.md) | `PUT /chats/status` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/update-chat-status-v1) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customerId` | [docs](https://docs.helpcrunch.com/en/rest-api-v1/update-customer-v1) |
