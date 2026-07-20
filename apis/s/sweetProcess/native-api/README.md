# SweetProcess: Native API Reference

A consolidated summary of SweetProcess's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/
- **API base URL:** `https://www.sweetprocess.com/api/v1`

## Authentication

### API key

Authenticate with a SweetProcess Legacy API Token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `results`.

## Pagination

Use `page_size` in the query string to set the page size (accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Invitation](actions/create-invitation.md) | `POST /invitations/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Create Team](actions/create-team.md) | `POST /teams/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Create User](actions/create-user.md) | `POST /users/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/:id/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Get Procedure](actions/get-procedure.md) | `GET /procedures/:id/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/y9C9fKdyD/integrating-sweetprocess-with-chatgpt-via-api/) |
| [List Procedures](actions/list-procedures.md) | `GET /procedures/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/y9C9fKdyD/integrating-sweetprocess-with-chatgpt-via-api/) |
| [List Taskinstances](actions/list-taskinstances.md) | `GET /taskinstances/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [List Teams](actions/list-teams.md) | `GET /teams/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [List Users](actions/list-users.md) | `GET /users/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
| [Update User](actions/update-user.md) | `PATCH /users/:id/` | [docs](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/) |
