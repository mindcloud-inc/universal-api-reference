# AWeber: Native API Reference

A consolidated summary of AWeber's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.aweber.com/
- **OpenAPI specification:** https://api.aweber.com/swagger.yaml
- **API base URL:** `https://api.aweber.com/1.0`

## Authentication

### OAuth 2.0

Connect AWeber with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.aweber.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.aweber.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account.read landing-page.read list.read list.write subscriber.read subscriber.write email.read email.write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.aweber.com/oauth2/token.

[Official authentication documentation](https://help.aweber.com/hc/en-us/articles/360021258174-How-do-I-use-OAuth-2-authentication-with-AWeber-s-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `entries`.

## Pagination

Use `ws.size` in the query string to set the page size (default 100; accepted range 1–100). Use `ws.start` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Field](actions/add-custom-field.md) | `POST /accounts/:accountId/lists/:listId/custom_fields` | [docs](https://api.aweber.com/#tag/Custom-Fields/paths/~1accounts~1{accountId}~1lists~1{listId}~1custom_fields/post) |
| [Add Subscriber](actions/add-subscriber.md) | `POST /accounts/:accountId/lists/:listId/subscribers` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers/post) |
| [Cancel Scheduled Broadcast](actions/cancel-scheduled-broadcast.md) | `POST /accounts/:accountId/lists/:listId/broadcasts/:broadcastId/cancel` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}~1cancel/post) |
| [Create Broadcast](actions/create-broadcast.md) | `POST /accounts/:accountId/lists/:listId/broadcasts` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts/post) |
| [Find Lists](actions/find-lists.md) | `GET /accounts/:accountId/lists` | [docs](https://api.aweber.com/#tag/Lists/paths/~1accounts~1{accountId}~1lists?ws.op=find/get) |
| [Find Subscribers For Account](actions/find-subscribers-for-account.md) | `GET /accounts/:accountId` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}?ws.op=findSubscribers/get) |
| [Find Subscribers For List](actions/find-subscribers-for-list.md) | `GET /accounts/:accountId/lists/:listId/subscribers` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers?ws.op=find/get) |
| [Get Account](actions/get-account.md) | `GET /accounts/:accountId` | [docs](https://api.aweber.com/#tag/Accounts/paths/~1accounts~1{accountId}/get) |
| [Get Broadcast](actions/get-broadcast.md) | `GET /accounts/:accountId/lists/:listId/broadcasts/:broadcastId` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}/get) |
| [Get Integration](actions/get-integration.md) | `GET /accounts/:accountId/integrations/:integrationId` | [docs](https://api.aweber.com/#tag/Integrations/paths/~1accounts~1{accountId}~1integrations~1{integrationId}/get) |
| [Get List](actions/get-list.md) | `GET /accounts/:accountId/lists/:listId` | [docs](https://api.aweber.com/#tag/Lists/paths/~1accounts~1{accountId}~1lists~1{listId}/get) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /accounts/:accountId/lists/:listId/subscribers/:subscriberId` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/get) |
| [Get Subscriber Activity](actions/get-subscriber-activity.md) | `GET /accounts/:accountId/lists/:listId/subscribers/:subscriberId` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}?ws.op=getActivity/get) |
| [Get Tags For List](actions/get-tags-for-list.md) | `GET /accounts/:accountId/lists/:listId/tags` | [docs](https://api.aweber.com/#tag/Lists/paths/~1accounts~1{accountId}~1lists~1{listId}~1tags/get) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://api.aweber.com/#tag/Accounts/paths/~1accounts/get) |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /accounts/:accountId/lists/:listId/broadcasts` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts/get) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /accounts/:accountId/lists/:listId/custom_fields` | [docs](https://api.aweber.com/#tag/Custom-Fields/paths/~1accounts~1{accountId}~1lists~1{listId}~1custom_fields/get) |
| [List Integrations](actions/list-integrations.md) | `GET /accounts/:accountId/integrations` | [docs](https://api.aweber.com/#tag/Integrations/paths/~1accounts~1{accountId}~1integrations/get) |
| [List Lists](actions/list-lists.md) | `GET /accounts/:accountId/lists` | [docs](https://api.aweber.com/#tag/Lists/paths/~1accounts~1{accountId}~1lists/get) |
| [List Subscribers](actions/list-subscribers.md) | `GET /accounts/:accountId/lists/:listId/subscribers` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers/get) |
| [Move Subscriber](actions/move-subscriber.md) | `POST /accounts/:accountId/lists/:listId/subscribers/:subscriberId` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/post) |
| [Schedule Broadcast](actions/schedule-broadcast.md) | `POST /accounts/:accountId/lists/:listId/broadcasts/:broadcastId/schedule` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}~1schedule/post) |
| [Update Broadcast](actions/update-broadcast.md) | `PUT /accounts/:accountId/lists/:listId/broadcasts/:broadcastId` | [docs](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}/put) |
| [Update Subscriber By ID](actions/update-subscriber-by-id.md) | `PATCH /accounts/:accountId/lists/:listId/subscribers/:subscriberId` | [docs](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/patch) |
