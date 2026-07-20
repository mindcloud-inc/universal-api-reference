# Zendesk: Native API Reference

A consolidated summary of Zendesk's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.zendesk.com/api-reference/
- **API base URL:** `https://{subdomain}.zendesk.com/api/v2`

## Authentication

### API token

Basic authentication using a Zendesk email address and API token.

### Credentials

- **Email address:** `username` · required
- **API token:** `password` · required
- **Subdomain:** `subdomain` · required · Zendesk account subdomain (for example, mindcloudhelp).

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.zendesk.com/hc/en-us/articles/4408889192858-Managing-API-token-access-to-the-Zendesk-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `tickets`.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group Membership](actions/create-group-membership.md) | `POST /group_memberships.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/groups/group_memberships/#create-membership) |
| [Create Organization](actions/create-organization.md) | `POST /organizations.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#create-organization) |
| [Create Organization Membership](actions/create-organization-membership.md) | `POST /organization_memberships.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organization_memberships/#create-membership) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#create-ticket) |
| [Create User](actions/create-user.md) | `POST /users.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#create-user) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /organizations/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#delete-organization) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#delete-ticket) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#delete-user) |
| [Execute View](actions/execute-view.md) | `GET /views/:view_id/execute.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/business-rules/views/#execute-view) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#show-self) |
| [Get Group](actions/get-group.md) | `GET /groups/:group_id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/groups/groups/#show-group) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#show-organization) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#show-ticket) |
| [Get User](actions/get-user.md) | `GET /users/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#show-user) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /group_memberships.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/groups/group_memberships/#list-memberships) |
| [List Groups](actions/list-groups.md) | `GET /groups.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/groups/groups/#list-groups) |
| [List Organization Memberships](actions/list-organization-memberships.md) | `GET /organization_memberships.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organization_memberships/#list-memberships) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#list-organizations) |
| [List Ticket Audits](actions/list-ticket-audits.md) | `GET /tickets/:ticket_id/audits.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_audits/#list-audits-for-a-ticket) |
| [List Ticket Comments](actions/list-ticket-comments.md) | `GET /tickets/:ticket_id/comments.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_comments/#list-comments) |
| [List Ticket Fields](actions/list-ticket-fields.md) | `GET /ticket_fields.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_fields/#list-ticket-fields) |
| [List Ticket Forms](actions/list-ticket-forms.md) | `GET /ticket_forms.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_forms/#list-ticket-forms) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#list-tickets) |
| [List Users](actions/list-users.md) | `GET /users.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#show-many-users) |
| [List Views](actions/list-views.md) | `GET /views.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/business-rules/views/#list-views) |
| [Search](actions/search.md) | `GET /search.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/ticket-management/search/#list-search-results) |
| [Search Users](actions/search-users.md) | `GET /users/search.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#search-users) |
| [Update Organization](actions/update-organization.md) | `PUT /organizations/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#update-organization) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#update-ticket) |
| [Update User](actions/update-user.md) | `PUT /users/:id.json` | [docs](https://developer.zendesk.com/api-reference/ticketing/users/users/#update-user) |
