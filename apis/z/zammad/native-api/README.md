# Zammad: Native API Reference

A consolidated summary of Zammad's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.zammad.org/en/latest/api/intro.html
- **API base URL:** `{baseUrl}/api/v1`

## Authentication

### API Token

Connect with a Zammad personal access token.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Your Zammad tenant URL, for example https://yourcompany.zammad.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.zammad.org/en/latest/api/user-access-token.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order_by`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://docs.zammad.org/en/latest/api/group.html) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://docs.zammad.org/en/latest/api/organization.html) |
| [Create Role](actions/create-role.md) | `POST /roles` | [docs](https://docs.zammad.org/en/latest/api/role.html) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://docs.zammad.org/en/latest/api/user.html) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://docs.zammad.org/en/latest/api/group.html) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /organizations/:id` | [docs](https://docs.zammad.org/en/latest/api/organization.html) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/:ticketId` | [docs](https://docs.zammad.org/en/latest/api/ticket/index.html) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://docs.zammad.org/en/latest/api/user.html#me-current-user) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://docs.zammad.org/en/latest/api/group.html) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:id` | [docs](https://docs.zammad.org/en/latest/api/organization.html) |
| [Get Role](actions/get-role.md) | `GET /roles/:id` | [docs](https://docs.zammad.org/en/latest/api/role.html) |
| [Get Ticket Priority](actions/get-ticket-priority.md) | `GET /ticket_priorities/:id` | [docs](https://docs.zammad.org/en/latest/api/ticket/priorities.html) |
| [Get Ticket State](actions/get-ticket-state.md) | `GET /ticket_states/:id` | [docs](https://docs.zammad.org/en/latest/api/ticket/states.html) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://docs.zammad.org/en/latest/api/user.html) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.zammad.org/en/latest/api/group.html) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://docs.zammad.org/en/latest/api/organization.html) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://docs.zammad.org/en/latest/api/role.html) |
| [List Ticket Priorities](actions/list-ticket-priorities.md) | `GET /ticket_priorities` | [docs](https://docs.zammad.org/en/latest/api/ticket/priorities.html) |
| [List Ticket States](actions/list-ticket-states.md) | `GET /ticket_states` | [docs](https://docs.zammad.org/en/latest/api/ticket/states.html) |
| [List Ticket Tags](actions/list-ticket-tags.md) | `GET /tags` | [docs](https://docs.zammad.org/en/latest/api/ticket/tags.html) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://docs.zammad.org/en/latest/api/ticket/index.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.zammad.org/en/latest/api/user.html) |
| [Search Tickets](actions/search-tickets.md) | `GET /tickets/search` | [docs](https://docs.zammad.org/en/latest/api/intro.html) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id` | [docs](https://docs.zammad.org/en/latest/api/group.html) |
| [Update Organization](actions/update-organization.md) | `PUT /organizations/:id` | [docs](https://docs.zammad.org/en/latest/api/organization.html) |
| [Update Role](actions/update-role.md) | `PUT /roles/:id` | [docs](https://docs.zammad.org/en/latest/api/role.html) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://docs.zammad.org/en/latest/api/user.html) |
