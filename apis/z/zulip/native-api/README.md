# Zulip: Native API Reference

A consolidated summary of Zulip's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://zulip.com/api/rest
- **API base URL:** `{site}/api/v1`

## Authentication

### Basic

Authenticate with a Zulip bot email, API key, and realm URL.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site URL:** `site` · required · Your Zulip server URL, for example https://your-org.zulipchat.com

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://zulip.com/api/http-headers)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Emoji Reaction](actions/add-emoji-reaction.md) | `POST /messages/:message_id/reactions` | [docs](https://zulip.com/api/add-reaction) |
| [Delete Event Queue](actions/delete-event-queue.md) | `DELETE /events` | [docs](https://zulip.com/api/delete-queue) |
| [Delete Message](actions/delete-message.md) | `DELETE /messages/:message_id` | [docs](https://zulip.com/api/delete-message) |
| [Edit Message](actions/edit-message.md) | `PATCH /messages/:message_id` | [docs](https://zulip.com/api/update-message) |
| [Fetch Single Message](actions/fetch-single-message.md) | `GET /messages/:message_id` | [docs](https://zulip.com/api/get-message) |
| [Get Channel by ID](actions/get-channel-by-id.md) | `GET /streams/:stream_id` | [docs](https://zulip.com/api/get-stream-by-id) |
| [Get Channel ID](actions/get-channel-id.md) | `GET /get_stream_id` | [docs](https://zulip.com/api/get-stream-id) |
| [Get Own User](actions/get-own-user.md) | `GET /users/me` | [docs](https://zulip.com/api/get-own-user) |
| [Get Server Settings](actions/get-server-settings.md) | `GET /server_settings` | [docs](https://zulip.com/api/get-server-settings) |
| [Get Subscription Status](actions/get-subscription-status.md) | `GET /users/:user_id/subscriptions/:stream_id` | [docs](https://zulip.com/api/get-subscription-status) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://zulip.com/api/get-user) |
| [Get User by Email](actions/get-user-by-email.md) | `GET /users/:email` | [docs](https://zulip.com/api/get-user-by-email) |
| [Get User Presence](actions/get-user-presence.md) | `GET /users/:user_id_or_email/presence` | [docs](https://zulip.com/api/get-user-presence) |
| [Get User Status](actions/get-user-status.md) | `GET /users/:user_id/status` | [docs](https://zulip.com/api/get-user-status) |
| [List Channel Subscribers](actions/list-channel-subscribers.md) | `GET /streams/:stream_id/members` | [docs](https://zulip.com/api/get-subscribers) |
| [List Channels](actions/list-channels.md) | `GET /streams` | [docs](https://zulip.com/api/get-streams) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://zulip.com/api/get-events) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://zulip.com/api/get-messages) |
| [List Subscribed Channels](actions/list-subscribed-channels.md) | `GET /users/me/subscriptions` | [docs](https://zulip.com/api/get-subscriptions) |
| [List Topics in a Channel](actions/list-topics-in-a-channel.md) | `GET /users/me/:stream_id/topics` | [docs](https://zulip.com/api/get-stream-topics) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://zulip.com/api/get-users) |
| [Register Event Queue](actions/register-event-queue.md) | `POST /register` | [docs](https://zulip.com/api/register-queue) |
| [Remove Emoji Reaction](actions/remove-emoji-reaction.md) | `DELETE /messages/:message_id/reactions` | [docs](https://zulip.com/api/remove-reaction) |
| [Render Message](actions/render-message.md) | `POST /messages/render` | [docs](https://zulip.com/api/render-message) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://zulip.com/api/send-message) |
