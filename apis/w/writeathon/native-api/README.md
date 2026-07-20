# Writeathon: Native API Reference

A consolidated summary of Writeathon's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://guide.writeathon.cn/help/tools/api.html
- **API base URL:** `https://api.writeathon.cn`

## Authentication

### Writeathon Token

Authenticate Writeathon requests with a user-generated integration token sent in the x-writeathon-token header.

### Credentials

- **API Key:** `apiKey` · required · Your Writeathon integration token from Settings > Integrations.
- **User ID:** `userId` · required · Your Writeathon user ID from Settings > Integrations.

Send these headers with each API request:

```http
x-writeathon-token: <apiKey>
```

[Official authentication documentation](https://guide.writeathon.cn/help/tools/api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append Card](actions/append-card.md) | `POST /v1/users/{{credentials.userId}}/cards` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Create Card](actions/create-card.md) | `POST /v1/users/{{credentials.userId}}/cards` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Create Card With Attachments](actions/create-card-with-attachments.md) | `POST /v1/users/{{credentials.userId}}/cards` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Extend Card](actions/extend-card.md) | `POST /v1/users/{{credentials.userId}}/cards/extend` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Extend Card With Attachments](actions/extend-card-with-attachments.md) | `POST /v1/users/{{credentials.userId}}/cards/extend` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Get Card By ID](actions/get-card-by-id.md) | `POST /v1/users/{{credentials.userId}}/cards/get` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Get Card By Title](actions/get-card-by-title.md) | `POST /v1/users/{{credentials.userId}}/cards/get` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Get Recent Cards](actions/get-recent-cards.md) | `GET /v1/users/{{credentials.userId}}/cards/recent` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [Get Writing Picks](actions/get-writing-picks.md) | `POST /v1/users/{{credentials.userId}}/writing-pick` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
| [List Spaces](actions/list-spaces.md) | `GET /v1/users/{{credentials.userId}}/spaces` | [docs](https://guide.writeathon.cn/help/tools/api.html) |
