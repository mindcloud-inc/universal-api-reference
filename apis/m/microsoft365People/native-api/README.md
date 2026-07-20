# Microsoft 365 People: Native API Reference

A consolidated summary of Microsoft 365 People's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access User.Read People.Read Contacts.ReadWrite`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /v1.0/me/contacts` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-contacts?view=graph-rest-1.0) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-delete?view=graph-rest-1.0) |
| [Get Contact](actions/get-contact.md) | `GET /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-get?view=graph-rest-1.0) |
| [List Contacts](actions/list-contacts.md) | `GET /v1.0/me/contacts` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-contacts?view=graph-rest-1.0) |
| [List People](actions/list-people.md) | `GET /v1.0/me/people` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-people?view=graph-rest-1.0) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-update?view=graph-rest-1.0) |
