# SupportBee: Native API Reference

A consolidated summary of SupportBee's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://supportbee.com/docs/api/reference
- **API base URL:** `https://{company}.supportbee.com`

## Authentication

### API Token

Connect to a SupportBee desk with an API token and desk subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Company:** `company` · required · Your SupportBee desk subdomain. For https://your-company.supportbee.com, enter your-company.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://supportbee.com/docs/api/reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–99). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Label to Ticket](actions/add-label-to-ticket.md) | `POST /tickets/:ticket_id/labels/:label_name` | [docs](https://supportbee.com/docs/api/reference#tag/Labels/paths/~1tickets~1{ticket_id}~1labels~1{label_name}/post) |
| [Archive Ticket](actions/archive-ticket.md) | `POST /tickets/:id/archive` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1archive/post) |
| [Assign Ticket to Team](actions/assign-ticket-to-team.md) | `POST /tickets/:id/team_assignment` | [docs](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1tickets~1{id}~1team_assignment/post) |
| [Assign Ticket to User](actions/assign-ticket-to-user.md) | `POST /tickets/:id/user_assignment` | [docs](https://supportbee.com/docs/api/reference#tag/Users/paths/~1tickets~1{id}~1user_assignment/post) |
| [Create Comment](actions/create-comment.md) | `POST /tickets/:id/comments` | [docs](https://supportbee.com/docs/api/reference#tag/Comments/paths/~1tickets~1{id}~1comments/post) |
| [Create Reply](actions/create-reply.md) | `POST /tickets/:id/replies` | [docs](https://supportbee.com/docs/api/reference#tag/Replies/paths/~1tickets~1{id}~1replies/post) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets/post) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:id` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}/get) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://supportbee.com/docs/api/reference#tag/Users/paths/~1users~1{id}/get) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://supportbee.com/docs/api/reference#tag/Labels/paths/~1labels/get) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1teams/get) |
| [List Ticket Comments](actions/list-ticket-comments.md) | `GET /tickets/:id/comments` | [docs](https://supportbee.com/docs/api/reference#tag/Comments/paths/~1tickets~1{id}~1comments/get) |
| [List Ticket Replies](actions/list-ticket-replies.md) | `GET /tickets/:id/replies` | [docs](https://supportbee.com/docs/api/reference#tag/Replies/paths/~1tickets~1{id}~1replies/get) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets/get) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://supportbee.com/docs/api/reference#tag/Users/paths/~1users/get) |
| [Mark Ticket Answered](actions/mark-ticket-answered.md) | `POST /tickets/:id/answered` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1answered/post) |
| [Mark Ticket as Spam](actions/mark-ticket-as-spam.md) | `POST /tickets/:id/spam` | [docs](https://supportbee.com/docs/api/reference#tag/Spam/paths/~1tickets~1{id}~1spam/post) |
| [Mark Ticket Unanswered](actions/mark-ticket-unanswered.md) | `DELETE /tickets/:id/answered` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1answered/delete) |
| [Restore Ticket](actions/restore-ticket.md) | `DELETE /tickets/:id/trash` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1trash/delete) |
| [Search Tickets](actions/search-tickets.md) | `GET /tickets/search` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1search/get) |
| [Trash Ticket](actions/trash-ticket.md) | `POST /tickets/:id/trash` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1trash/post) |
| [Unarchive Ticket](actions/unarchive-ticket.md) | `DELETE /tickets/:id/archive` | [docs](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1{id}~1archive/delete) |
| [Unassign Ticket from Team](actions/unassign-ticket-from-team.md) | `DELETE /tickets/:id/team_assignment` | [docs](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1tickets~1{id}~1team_assignment/delete) |
| [Unassign Ticket from User](actions/unassign-ticket-from-user.md) | `DELETE /tickets/:id/user_assignment` | [docs](https://supportbee.com/docs/api/reference#tag/Users/paths/~1tickets~1{id}~1user_assignment/delete) |
