# Pusher: Native API Reference

A consolidated summary of Pusher's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://pusher.com/docs/channels/library_auth_reference/rest-api/
- **API base URL:** `https://api-{cluster}.pusher.com`

## Authentication

### Pusher Channels HMAC

Use the Pusher Channels app credentials required for HMAC-signed server API requests.

### Credentials

- **App ID:** `appId` · required · Pusher Channels app ID used in the request path and signing string.
- **Key:** `key` · required · Pusher Channels app key used as auth_key in signed requests.
- **Secret:** `secret` · required · Pusher Channels app secret used to compute the HMAC SHA256 auth_signature.
- **Cluster:** `cluster` · required · Pusher Channels cluster, for example mt1, used to build the API hostname.

[Official authentication documentation](https://pusher.com/docs/channels/library_auth_reference/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | `GET /apps/{{credentials.appId}}/channels/:channel_name` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-channel-fetch-info-for-one-channel) |
| [List Channel Users](actions/list-channel-users.md) | `GET /apps/{{credentials.appId}}/channels/:channel_name/users` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-users) |
| [List Channels](actions/list-channels.md) | `GET /apps/{{credentials.appId}}/channels` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-channels-fetch-info-for-multiple-channels) |
| [Terminate User Connections](actions/terminate-user-connections.md) | `POST /apps/{{credentials.appId}}/users/:user_id/terminate_connections` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-terminate-user-connections) |
| [Trigger Batch Events](actions/trigger-batch-events.md) | `POST /apps/{{credentials.appId}}/batch_events` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-batch-events-trigger-multiple-events) |
| [Trigger Event](actions/trigger-event.md) | `POST /apps/{{credentials.appId}}/events` | [docs](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-event-trigger-an-event) |
