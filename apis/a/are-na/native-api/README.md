# Are.na: Native API Reference

A consolidated summary of Are.na's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.are.na/developers/explore
- **OpenAPI specification:** https://api.are.na/v3/openapi.json
- **API base URL:** `https://api.are.na/v3`

## Authentication

### Personal Access Token

Authenticate with an Are.na personal access token or OAuth access token using the Bearer token format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.are.na/developers/explore)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `input.meta.next_page`. The total page count is read from `input.meta.total_pages`. The current page number is read from `input.meta.current_page`.

## Pagination

Use `per` in the query string to set the page size (default 24; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Block](actions/create-block.md) | `POST blocks` | [docs](https://www.are.na/developers/explore/block/post-block) |
| [Create Block Comment](actions/create-block-comment.md) | `POST blocks/:id/comments` | [docs](https://www.are.na/developers/explore/block/post-comments) |
| [Create Channel](actions/create-channel.md) | `POST channels` | [docs](https://www.are.na/developers/explore/channel/post-channel) |
| [Create Connection](actions/create-connection.md) | `POST connections` | [docs](https://www.are.na/developers/explore/connection/post-connection) |
| [Create Upload Presign URL](actions/create-upload-presign-url.md) | `POST uploads/presign` | [docs](https://www.are.na/developers/explore/upload/post-presign) |
| [Delete Channel](actions/delete-channel.md) | `DELETE channels/:id` | [docs](https://www.are.na/developers/explore/channel/delete-channel) |
| [Delete Comment](actions/delete-comment.md) | `DELETE comments/:id` | [docs](https://www.are.na/developers/explore/comment/delete-comment) |
| [Delete Connection](actions/delete-connection.md) | `DELETE connections/:id` | [docs](https://www.are.na/developers/explore/connection/delete-connection) |
| [Get Block](actions/get-block.md) | `GET blocks/:id` | [docs](https://www.are.na/developers/explore/block) |
| [Get Channel](actions/get-channel.md) | `GET channels/:id` | [docs](https://www.are.na/developers/explore/channel) |
| [Get Connection](actions/get-connection.md) | `GET connections/:id` | [docs](https://www.are.na/developers/explore/connection) |
| [Get Current User](actions/get-current-user.md) | `GET me` | [docs](https://www.are.na/developers/explore/user/me) |
| [Get Group](actions/get-group.md) | `GET groups/:id` | [docs](https://www.are.na/developers/explore/group) |
| [Get OpenAPI Specification](actions/get-open-api-specification.md) | `GET openapi.json` | [docs](https://www.are.na/developers/explore/system/openapi-json) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://www.are.na/developers/explore/user) |
| [List Block Comments](actions/list-block-comments.md) | `GET blocks/:id/comments` | [docs](https://www.are.na/developers/explore/block/comments) |
| [List Block Connections](actions/list-block-connections.md) | `GET blocks/:id/connections` | [docs](https://www.are.na/developers/explore/block/connections) |
| [List Channel Connections](actions/list-channel-connections.md) | `GET channels/:id/connections` | [docs](https://www.are.na/developers/explore/channel/connections) |
| [List Channel Contents](actions/list-channel-contents.md) | `GET channels/:id/contents` | [docs](https://www.are.na/developers/explore/channel/contents) |
| [List Channel Followers](actions/list-channel-followers.md) | `GET channels/:id/followers` | [docs](https://www.are.na/developers/explore/channel/followers) |
| [List Group Contents](actions/list-group-contents.md) | `GET groups/:id/contents` | [docs](https://www.are.na/developers/explore/group/contents) |
| [List Group Followers](actions/list-group-followers.md) | `GET groups/:id/followers` | [docs](https://www.are.na/developers/explore/group/followers) |
| [List User Contents](actions/list-user-contents.md) | `GET users/:id/contents` | [docs](https://www.are.na/developers/explore/user/contents) |
| [List User Followers](actions/list-user-followers.md) | `GET users/:id/followers` | [docs](https://www.are.na/developers/explore/user/followers) |
| [List User Following](actions/list-user-following.md) | `GET users/:id/following` | [docs](https://www.are.na/developers/explore/user/following) |
| [List User Groups](actions/list-user-groups.md) | `GET users/:id/groups` | [docs](https://www.are.na/developers/explore/user/groups) |
| [Move Connection](actions/move-connection.md) | `POST connections/:id/move` | [docs](https://www.are.na/developers/explore/connection/post-move) |
| [Ping](actions/ping.md) | `GET ping` | [docs](https://www.are.na/developers/explore/system/ping) |
| [Search Are.na](actions/search-arena.md) | `GET search` | [docs](https://www.are.na/developers/explore/search) |
| [Update Block](actions/update-block.md) | `PUT blocks/:id` | [docs](https://www.are.na/developers/explore/block/put-block) |
| [Update Channel](actions/update-channel.md) | `PUT channels/:id` | [docs](https://www.are.na/developers/explore/channel/put-channel) |
| [Update Connection](actions/update-connection.md) | `PUT connections/:id` | [docs](https://www.are.na/developers/explore/connection/put-connection) |
