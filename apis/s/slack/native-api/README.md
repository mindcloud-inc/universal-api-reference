# Slack: Native API Reference

A consolidated summary of Slack's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.slack.dev/reference/methods/
- **API base URL:** `https://slack.com/api/`

## Authentication

### OAuth2

### Credentials

- **Default Sender:** `defaultSender` · optional · Would you like Slack to act as yourself or a bot?

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://slack.com/oauth/v2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://slack.com/api/oauth.v2.access.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `channels:manage channels:read channels:join chat:write chat:write.customize chat:write.public commands files:read files:write im:write mpim:write search:read.public search:read.users team:read users.profile:read users:read users:read.email users:write reactions:read reactions:write groups:history groups:read groups:write`.

The flow supports refresh tokens.

[Official authentication documentation](https://api.slack.com/legacy/oauth)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Wait 3000 ms before the first retry. Stop after 5 attempts.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Reaction](actions/add-reaction.md) | `POST reactions.add` | [docs](https://docs.slack.dev/reference/methods/reactions.add/) |
| [Create Channel](actions/create-channel.md) | `POST conversations.create` | [docs](https://docs.slack.dev/reference/methods/conversations.create/) |
| [Delete File](actions/delete-file.md) | `POST files.delete` | [docs](https://docs.slack.dev/reference/methods/files.delete/) |
| [Delete Message](actions/delete-message.md) | `POST chat.delete` | [docs](https://docs.slack.dev/reference/methods/chat.delete/) |
| [Delete Scheduled Message](actions/delete-scheduled-message.md) | `POST chat.deleteScheduledMessage` | [docs](https://docs.slack.dev/reference/methods/chat.deleteScheduledMessage/) |
| [Get Channel Information](actions/get-channel-information.md) | `GET conversations.info` | [docs](https://docs.slack.dev/reference/methods/conversations.info/) |
| [Get File Information](actions/get-file-information.md) | `GET files.info` | [docs](https://docs.slack.dev/reference/methods/files.info/) |
| [Get User Information](actions/get-user-information.md) | `GET users.info` | [docs](https://docs.slack.dev/reference/methods/users.info/) |
| [Invite User to Channel](actions/invite-user-to-channel.md) | `POST conversations.invite` | [docs](https://docs.slack.dev/reference/methods/conversations.invite/) |
| [Join Channel](actions/join-channel.md) | `GET conversations.join` | [docs](https://docs.slack.dev/reference/methods/conversations.join/) |
| [Kick User From Channel](actions/kick-user-from-channel.md) | `POST conversations.kick` | [docs](https://docs.slack.dev/reference/methods/conversations.kick/) |
| [Leave Channel](actions/leave-channel.md) | `POST conversations.leave` | [docs](https://docs.slack.dev/reference/methods/conversations.leave/) |
| [List Channel Members](actions/list-channel-members.md) | `GET conversations.members` | [docs](https://docs.slack.dev/reference/methods/conversations.members/) |
| [List Channel Messages](actions/list-channel-messages.md) | `POST conversations.history` | [docs](https://docs.slack.dev/reference/methods/conversations.history/) |
| [List Channels](actions/list-channels.md) | `GET conversations.list` | [docs](https://docs.slack.dev/reference/methods/conversations.list/) |
| [List Files](actions/list-files.md) | `GET files.list` | [docs](https://docs.slack.dev/reference/methods/files.list/) |
| [List Message Reactions](actions/list-message-reactions.md) | `GET reactions.get` | [docs](https://docs.slack.dev/reference/methods/reactions.get/) |
| [List Message Replies](actions/list-message-replies.md) | `GET conversations.replies` | [docs](https://docs.slack.dev/reference/methods/conversations.replies/) |
| [List Scheduled Messages](actions/list-scheduled-messages.md) | `POST chat.scheduledMessages.list` | [docs](https://docs.slack.dev/reference/methods/chat.scheduledMessages.list/) |
| [List User Reactions](actions/list-user-reactions.md) | `GET reactions.list` | [docs](https://docs.slack.dev/reference/methods/reactions.list/) |
| [List Users](actions/list-users.md) | `GET users.list` | [docs](https://docs.slack.dev/reference/methods/users.list/) |
| [Open Conversation](actions/open-conversation.md) | `POST conversations.open` | [docs](https://docs.slack.dev/reference/methods/conversations.open/) |
| [Remove Reaction](actions/remove-reaction.md) | `POST reactions.remove` | [docs](https://docs.slack.dev/reference/methods/reactions.remove/) |
| [Schedule Message](actions/schedule-message.md) | `POST chat.scheduleMessage` | [docs](https://docs.slack.dev/reference/methods/chat.scheduleMessage/) |
| [Search Channels and Users](actions/search-channels-and-users.md) | `POST assistant.search.context` | [docs](https://docs.slack.dev/reference/methods/assistant.search.context/) |
| [Search User By Email](actions/search-user-by-email.md) | `GET users.lookupByEmail` | [docs](https://docs.slack.dev/reference/methods/users.lookupByEmail/) |
| [Send Channel Message](actions/send-channel-message.md) | `POST chat.postMessage` | [docs](https://docs.slack.dev/reference/methods/chat.postMessage/) |
| [Send User Message](actions/send-user-message.md) | `POST chat.postMessage` | [docs](https://docs.slack.dev/reference/methods/chat.postMessage/) |
| [Set Channel Topic](actions/set-channel-topic.md) | `POST conversations.setTopic` | [docs](https://docs.slack.dev/reference/methods/conversations.setTopic/) |
| [Set Presence](actions/set-status.md) | `POST users.setPresence` | [docs](https://docs.slack.dev/reference/methods/users.setPresence/) |
| [Update Message](actions/update-message.md) | `POST chat.update` | [docs](https://docs.slack.dev/reference/methods/chat.update/) |
