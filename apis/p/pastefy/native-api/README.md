# Pastefy: Native API Reference

A consolidated summary of Pastefy's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.pastefy.app/api
- **API base URL:** `https://pastefy.app/api/v2`

## Authentication

### API Token

Use a Pastefy API token generated from the API Keys page in Pastefy.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pastefy.app/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | `POST /user/keys` | [docs](https://docs.pastefy.app/api/spec/post-user-keys.html) |
| [Create Folder](actions/create-folder.md) | `POST /folder` | [docs](https://docs.pastefy.app/api/spec/post-folder.html) |
| [Create Paste](actions/create-paste.md) | `POST /paste` | [docs](https://docs.pastefy.app/api/spec/post-paste.html) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /user/keys/:id` | [docs](https://docs.pastefy.app/api/spec/delete-user-keys-%7Bid%7D.html) |
| [Delete Paste](actions/delete-paste.md) | `DELETE /paste/:id` | [docs](https://docs.pastefy.app/api/spec/delete-paste-%7Bid%7D.html) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://docs.pastefy.app/api/spec/get-user.html) |
| [Get Paste](actions/get-paste.md) | `GET /paste/:id` | [docs](https://docs.pastefy.app/api/spec/get-paste-%7Bid%7D.html) |
| [Get Paste Raw Content](actions/get-paste-raw-content.md) | `GET https://pastefy.app/:id/raw` | [docs](https://docs.pastefy.app/api/spec/get-paste-%7Bid%7D-raw.html) |
| [Get User Overview](actions/get-user-overview.md) | `GET /user/overview` | [docs](https://docs.pastefy.app/api/spec/get-user-overview.html) |
| [List API Keys](actions/list-api-keys.md) | `GET /user/keys` | [docs](https://docs.pastefy.app/api/spec/get-user-keys.html) |
| [List Folders](actions/list-folders.md) | `GET /folder` | [docs](https://docs.pastefy.app/api/spec/get-folder.html) |
| [List Pastes](actions/list-pastes.md) | `GET /paste` | [docs](https://docs.pastefy.app/api/spec/get-paste.html) |
| [List Starred Pastes](actions/list-starred-pastes.md) | `GET /user/starred-pastes` | [docs](https://docs.pastefy.app/api/spec/get-user-starred-pastes.html) |
| [List Trending Public Pastes](actions/list-trending-public-pastes.md) | `GET /public-pastes/trending` | [docs](https://docs.pastefy.app/api/spec/get-public-pastes-trending.html) |
| [List User Pastes](actions/list-user-pastes.md) | `GET /user/pastes` | [docs](https://docs.pastefy.app/api/spec/get-user-pastes.html) |
| [Star Paste](actions/star-paste.md) | `POST /paste/:id/star` | [docs](https://docs.pastefy.app/api/spec/post-paste-%7Bid%7D-star.html) |
| [Unstar Paste](actions/unstar-paste.md) | `DELETE /paste/:id/star` | [docs](https://docs.pastefy.app/api/spec/delete-paste-%7Bid%7D-star.html) |
| [Update Paste](actions/update-paste.md) | `PUT /paste/:id` | [docs](https://docs.pastefy.app/api/spec/put-paste-%7Bid%7D.html) |
