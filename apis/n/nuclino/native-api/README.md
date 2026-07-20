# Nuclino: Native API Reference

A consolidated summary of Nuclino's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://help.nuclino.com/d3a29686-api
- **API base URL:** `https://api.nuclino.com/v0`

## Authentication

### API Key

Authenticate with a Nuclino API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.nuclino.com/04598850-manage-api-keys)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `after` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create item or collection](actions/create-item-or-collection.md) | `POST /items` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
| [Delete item or collection](actions/delete-item-or-collection.md) | `DELETE /items/:id` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
| [Get file](actions/get-file.md) | `GET /files/:id` | [docs](https://help.nuclino.com/9a737add-files) |
| [Get item or collection](actions/get-item-or-collection.md) | `GET /items/:id` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
| [Get team](actions/get-team.md) | `GET /teams/:id` | [docs](https://help.nuclino.com/b72e5fdd-teams) |
| [Get user](actions/get-user.md) | `GET /users/:id` | [docs](https://help.nuclino.com/f76dc920-users) |
| [Get workspace](actions/get-workspace.md) | `GET /workspaces/:id` | [docs](https://help.nuclino.com/702467a8-workspaces) |
| [List items and collections](actions/list-items-and-collections.md) | `GET /items` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
| [List teams](actions/list-teams.md) | `GET /teams` | [docs](https://help.nuclino.com/b72e5fdd-teams) |
| [List workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://help.nuclino.com/702467a8-workspaces) |
| [Search items and collections](actions/search-items-and-collections.md) | `GET /items` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
| [Update item or collection](actions/update-item-or-collection.md) | `PUT /items/:id` | [docs](https://help.nuclino.com/fa38d15f-items-and-collections) |
