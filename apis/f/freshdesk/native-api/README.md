# Freshdesk: Native API Reference

A consolidated summary of Freshdesk's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.freshdesk.com/api/
- **API base URL:** `https://{subdomain}.freshdesk.com/api/v2`

## Authentication

### Basic

Authenticate with Freshdesk API key using HTTP Basic auth (API key as username, X as password).

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Subdomain:** `subdomain` · required · Your Freshdesk account subdomain (for https://<subdomain>.freshdesk.com).

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.freshdesk.com/api/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_type`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://developers.freshdesk.com/api/#create_company) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.freshdesk.com/api/#create_contact) |
| [Create Note](actions/create-note.md) | `POST /tickets/:ticketId/notes` | [docs](https://developers.freshdesk.com/api/#add_note_to_a_ticket) |
| [Create Reply](actions/create-reply.md) | `POST /tickets/:id/reply` | [docs](https://developers.freshdesk.com/api/#reply_ticket) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://developers.freshdesk.com/api/#create_ticket) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/:id` | [docs](https://developers.freshdesk.com/api/#delete_company) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/:id` | [docs](https://developers.freshdesk.com/api/#delete_a_ticket) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:id` | [docs](https://developers.freshdesk.com/api/#view_agent) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://developers.freshdesk.com/api/#view_company) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.freshdesk.com/api/#view_contact) |
| [Get Currently Authenticated Agent](actions/get-currently-authenticated-agent.md) | `GET /agents/me` | [docs](https://developers.freshdesk.com/api/#me) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:id` | [docs](https://developers.freshdesk.com/api/#view_a_ticket) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://developers.freshdesk.com/api/#list_all_agents) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developers.freshdesk.com/api/#list_all_companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.freshdesk.com/api/#list_all_contacts) |
| [List Ticket Conversations](actions/list-ticket-conversations.md) | `GET /tickets/:id/conversations` | [docs](https://developers.freshdesk.com/api/#list_all_ticket_notes) |
| [List Ticket Time Entries](actions/list-ticket-time-entries.md) | `GET /tickets/:id/time_entries` | [docs](https://developers.freshdesk.com/api/#list_all_ticket_timeentries) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://developers.freshdesk.com/api/#list_all_tickets) |
| [Search Tickets](actions/search-tickets.md) | `GET /search/tickets` | [docs](https://developers.freshdesk.com/api/#filter_tickets) |
| [Soft Delete a Contact](actions/soft-delete-a-contact.md) | `DELETE /contacts/:id` | [docs](https://developers.freshdesk.com/api/#delete_contact) |
| [Update Company](actions/update-company.md) | `PUT /companies/:id` | [docs](https://developers.freshdesk.com/api/#update_company) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developers.freshdesk.com/api/#update_contact) |
| [Update Conversation](actions/update-conversation.md) | `PUT /conversations/:id` | [docs](https://developers.freshdesk.com/api/#update_conversation) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:id` | [docs](https://developers.freshdesk.com/api/#update_ticket) |
