# Pushbullet: Native API Reference

A consolidated summary of Pushbullet's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.pushbullet.com/v8/
- **API base URL:** `https://api.pushbullet.com/v2`

## Authentication

### OAuth2

Authenticate via Pushbullet OAuth2 authorization flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.pushbullet.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.pushbullet.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://docs.pushbullet.com/v8/#oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `cursor`.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | `POST /chats` |  |
| [Create Device](actions/create-device.md) | `POST /devices` | [docs](https://docs.pushbullet.com/v8/#devices) |
| [Create Push](actions/create-push.md) | `POST /pushes` | [docs](https://docs.pushbullet.com/v8/#pushes) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://docs.pushbullet.com/v8/#subscriptions) |
| [Create Upload Request](actions/create-upload-request.md) | `POST /upload-request` | [docs](https://docs.pushbullet.com/v8/#upload-request) |
| [Delete All Pushes](actions/delete-all-pushes.md) | `DELETE /pushes` | [docs](https://docs.pushbullet.com/v8/#pushes) |
| [Delete Chat](actions/delete-chat.md) | `DELETE /chats/:chat_iden` |  |
| [Delete Device](actions/delete-device.md) | `DELETE /devices/:device_iden` | [docs](https://docs.pushbullet.com/v8/#devices) |
| [Delete Push](actions/delete-push.md) | `DELETE /pushes/:push_iden` | [docs](https://docs.pushbullet.com/v8/#pushes) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /subscriptions/:iden` | [docs](https://docs.pushbullet.com/v8/#subscriptions) |
| [Get Channel Info](actions/get-channel-info.md) | `GET /channel-info` | [docs](https://docs.pushbullet.com/v8/#subscriptions) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://docs.pushbullet.com/v8/#users) |
| [List Chats](actions/list-chats.md) | `GET /chats` |  |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://docs.pushbullet.com/v8/#devices) |
| [List Pushes](actions/list-pushes.md) | `GET /pushes` | [docs](https://docs.pushbullet.com/v8/#pushes) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://docs.pushbullet.com/v8/#subscriptions) |
| [Send Ephemeral](actions/send-ephemeral.md) | `POST /ephemerals` | [docs](https://docs.pushbullet.com/v8/#ephemerals) |
| [Update Chat](actions/update-chat.md) | `POST /chats/:chat_iden` |  |
| [Update Device](actions/update-device.md) | `POST /devices/:device_iden` | [docs](https://docs.pushbullet.com/v8/#devices) |
| [Update Push](actions/update-push.md) | `POST /pushes/:push_iden` | [docs](https://docs.pushbullet.com/v8/#pushes) |
