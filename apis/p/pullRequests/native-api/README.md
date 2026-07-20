# 24 Pull Requests: Native API Reference

A consolidated summary of 24 Pull Requests's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://24pullrequests.com/api
- **API base URL:** `https://24pullrequests.com`

## Authentication

### No authentication

24 Pull Requests public JSON API does not require credentials for documented GET endpoints.

This API does not require request authentication.

[Official authentication documentation](https://24pullrequests.com/api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Contributions Metadata](actions/get-contributions-metadata.md) | `GET /pull_requests/meta.json` | [docs](https://24pullrequests.com/api) |
| [Get Organisation](actions/get-organisation.md) | `GET /organisations/:login.json` | [docs](https://24pullrequests.com/api) |
| [Get User](actions/get-user.md) | `GET /users/:nickname.json` | [docs](https://24pullrequests.com/api) |
| [List Contributions](actions/list-contributions.md) | `GET /pull_requests.json` | [docs](https://24pullrequests.com/api) |
| [List Organisations](actions/list-organisations.md) | `GET /organisations.json` | [docs](https://24pullrequests.com/api) |
| [List Projects](actions/list-projects.md) | `GET /projects.json` | [docs](https://24pullrequests.com/api) |
| [List Users](actions/list-users.md) | `GET /users.json` | [docs](https://24pullrequests.com/api) |
