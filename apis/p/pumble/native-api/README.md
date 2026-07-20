# Pumble: Native API Reference

A consolidated summary of Pumble's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://pumble-api-keys.addons.marketplace.cake.com/api-docs/
- **API base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`

## Authentication

### API Key (Custom Header)

Connect with a Pumble API key and send it through the required ApiKey header.

### Credentials

- **API Key:** `apiKey` · required · The Pumble API key generated from the API addon.

[Official authentication documentation](https://pumble.com/help/integrations/automation-workflow-integrations/api-keys-integration/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Reaction to Message](actions/add-reaction-to-message.md) | `POST /addReaction` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Add Users to Channel](actions/add-users-to-channel.md) | `POST /addUsersToChannel` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Create Channel](actions/create-channel.md) | `POST /createChannel` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Create Scheduled Message](actions/create-scheduled-message.md) | `POST /createScheduledMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Delete Message](actions/delete-message.md) | `DELETE /deleteMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Delete Scheduled Message](actions/delete-scheduled-message.md) | `DELETE /deleteScheduledMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Get Channel](actions/get-channel.md) | `GET /getChannel` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Get Current User](actions/get-current-user.md) | `GET /myInfo` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Get Message](actions/get-message.md) | `GET /fetchMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Get Scheduled Message](actions/get-scheduled-message.md) | `GET /fetchScheduledMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /listMessages` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List Channels](actions/list-channels.md) | `GET /listChannels` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List Scheduled Messages](actions/list-scheduled-messages.md) | `GET /fetchScheduledMessages` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List Thread Replies](actions/list-thread-replies.md) | `GET /fetchThreadReplies` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List User Groups](actions/list-user-groups.md) | `GET /listUserGroups` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [List Users](actions/list-users.md) | `GET /listUsers` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Remove User from Channel](actions/remove-user-from-channel.md) | `POST /removeUserFromChannel` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Reply to Message](actions/reply-to-message.md) | `POST /sendReply` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Search Messages](actions/search-messages.md) | `POST /searchMessages` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Send Direct Message to Group](actions/send-direct-message-to-group.md) | `POST /dmGroup` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Send Direct Message to User](actions/send-direct-message-to-user.md) | `POST /dmUser` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Send Message to Channel](actions/send-message-to-channel.md) | `POST /sendMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Update Message](actions/update-message.md) | `POST /editMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
| [Update Scheduled Message](actions/update-scheduled-message.md) | `POST /editScheduledMessage` | [docs](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/) |
