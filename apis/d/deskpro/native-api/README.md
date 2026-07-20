# Deskpro: Native API Reference

A consolidated summary of Deskpro's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.deskpro.com/developers/api-docs/v2.html
- **API base URL:** `{helpdeskUrl}/api/v2`

## Authentication

### OAuth 2.0

OAuth 2.0 authorization code flow for Deskpro API access.

### Credentials

- **Helpdesk URL:** `helpdeskUrl` · required · Full Deskpro helpdesk root URL without a trailing slash, for example https://your-helpdesk.deskpro.com
- **Auth Endpoint:** `authEndpoint` · required · Full Deskpro OAuth authorization endpoint copied from Deskpro Admin -> Apps -> OAuth -> your client details. Example pattern from Deskpro docs: https://your-helpdesk.example/api/v2/oauth/agent/<clientRecordId>
- **Token Endpoint:** `tokenEndpoint` · required · Full Deskpro OAuth token endpoint copied from Deskpro Admin -> Apps -> OAuth -> your client details. Deskpro's official OAuth screenshot shows a token endpoint ending in /api/v2/oauth/token.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.authEndpoint}} to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.tokenEndpoint}}.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Basic`.

[Official authentication documentation](https://deskpro.gitbook.io/dev-guide/api-basics/auth/api-tokens/oauth)

### API Key

Deskpro API key authentication using the Authorization header format required by Deskpro.

### Credentials

- **API Key:** `apiKey` · required
- **Helpdesk URL:** `helpdeskUrl` · required · Full Deskpro helpdesk root URL without a trailing slash, for example https://mindcloud.deskpro.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.deskpro.com/en-US/kb/articles/pdf/basic-api-usage)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.pagination.total_pages`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `count` in the query string to set the page size (default 50; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-agents-{id}) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-me) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organizationId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-organizations-{id}) |
| [Get Person](actions/get-person.md) | `GET /people/:id` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-people-{id}) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:ticketId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{id}) |
| [Get Ticket Filter](actions/get-ticket-filter.md) | `GET /ticket_filters/:ticketFilterId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-ticket_filters-{id}) |
| [Get Ticket Filter Count](actions/get-ticket-filter-count.md) | `GET /ticket_filters/:ticketFilterId/count` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-ticket_filters-{id}-count) |
| [Get Ticket Log](actions/get-ticket-log.md) | `GET /tickets/:ticketId/logs/:logId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-logs-{id}) |
| [Get Ticket Message](actions/get-ticket-message.md) | `GET /tickets/:ticketId/messages/:messageId` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-messages-{id}) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-agents) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-articles) |
| [List Guides](actions/list-guides.md) | `GET /guides` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-guides) |
| [List Online Agents](actions/list-online-agents.md) | `GET /agents/online` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-agents-online) |
| [List Organization Tickets](actions/list-organization-tickets.md) | `GET /organizations/:organizationId/tickets` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-organizations-{id}-tickets) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-organizations) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-people) |
| [List Person Tickets](actions/list-person-tickets.md) | `GET /people/:personId/tickets` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-people-{id}-tickets) |
| [List Ticket Approvals](actions/list-ticket-approvals.md) | `GET /tickets/:ticketId/ticket_approvals` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{ticketId}-ticket_approvals) |
| [List Ticket Filter Tickets](actions/list-ticket-filter-tickets.md) | `GET /ticket_filters/:ticketFilterId/tickets` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-ticket_filters-{ticketFilter}-tickets) |
| [List Ticket Filters](actions/list-ticket-filters.md) | `GET /ticket_filters` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-ticket_filters) |
| [List Ticket IDs](actions/list-ticket-ids.md) | `GET /tickets/ids` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-ids) |
| [List Ticket Logs](actions/list-ticket-logs.md) | `GET /tickets/:ticketId/logs` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-logs) |
| [List Ticket Messages](actions/list-ticket-messages.md) | `GET /tickets/:ticketId/messages` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets-{parentId}-messages) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-tickets) |
