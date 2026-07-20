# NeetoDesk: Native API Reference

A consolidated summary of NeetoDesk's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.neetodesk.com
- **API base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`

## Authentication

### API key

Authenticate NeetoDesk requests with a workspace-specific API key.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Subdomain:** `workspaceSubdomain` · required · Enter your NeetoDesk workspace subdomain only, without .neetodesk.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.neetodesk.com/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `team_members`. The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.current_page_number`.

## Pagination

Use `page_size` in the query string to set the page size (default 30). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | `POST /team-members` | [docs](https://apidocs.neetodesk.com/api-reference/team-members/add) |
| [Create Comment](actions/create-comment.md) | `POST /tickets/:ticket_id/comments` | [docs](https://apidocs.neetodesk.com/api-reference/comments/create) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://apidocs.neetodesk.com/api-reference/customers/create) |
| [Create Draft Comment](actions/create-draft-comment.md) | `POST /tickets/:ticket_id/drafts` | [docs](https://apidocs.neetodesk.com/api-reference/comments/create-draft) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://apidocs.neetodesk.com/api-reference/tickets/create) |
| [Get Agent Performance Report](actions/get-agent-performance-report.md) | `GET /reports/agents` | [docs](https://apidocs.neetodesk.com/api-reference/reports/get-agent-performance) |
| [Get Comment](actions/get-comment.md) | `GET /tickets/:ticket_id/comments/:comment_id` | [docs](https://apidocs.neetodesk.com/api-reference/comments/get) |
| [Get Customer Satisfaction Report](actions/get-customer-satisfaction-report.md) | `GET /reports/surveys` | [docs](https://apidocs.neetodesk.com/api-reference/reports/get-customer-satisfaction) |
| [Get Team Member Details](actions/get-team-member-details.md) | `GET /team-members/:team_member_id` | [docs](https://apidocs.neetodesk.com/api-reference/team-members/get) |
| [Get Team Performance Report](actions/get-team-performance-report.md) | `GET /reports/groups` | [docs](https://apidocs.neetodesk.com/api-reference/reports/get-team-performance) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:ticket_id` | [docs](https://apidocs.neetodesk.com/api-reference/tickets/get) |
| [Get Ticket Volume Report](actions/get-ticket-volume-report.md) | `GET /reports/tickets` | [docs](https://apidocs.neetodesk.com/api-reference/reports/get-ticket-volume) |
| [Get Ticket Volume Time Series](actions/get-ticket-volume-time-series.md) | `GET /reports/ticket-time-series` | [docs](https://apidocs.neetodesk.com/api-reference/reports/get-ticket-time-series) |
| [List Comments](actions/list-comments.md) | `GET /tickets/:ticket_id/comments` | [docs](https://apidocs.neetodesk.com/api-reference/comments/list) |
| [List Team Members](actions/list-team-members.md) | `GET /team-members` | [docs](https://apidocs.neetodesk.com/api-reference/team-members/list) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://apidocs.neetodesk.com/api-reference/tickets/list) |
| [Remove Team Member](actions/remove-team-member.md) | `DELETE /team-members/:team_member_id` | [docs](https://apidocs.neetodesk.com/api-reference/team-members/remove) |
| [Update Team Member](actions/update-team-member.md) | `PATCH /team-members/:team_member_id` | [docs](https://apidocs.neetodesk.com/api-reference/team-members/update) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:ticket_id` | [docs](https://apidocs.neetodesk.com/api-reference/tickets/update) |
