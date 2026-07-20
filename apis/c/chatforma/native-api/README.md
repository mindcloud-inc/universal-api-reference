# Chatforma: Native API Reference

A consolidated summary of Chatforma's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.chatforma.com/
- **OpenAPI specification:** https://docs.chatforma.com/docs/chatforma.json
- **API base URL:** `https://api.pro.chatforma.com/public/v1`

## Authentication

### API Key

Connect with a Chatforma integration token from Profile -> Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://learn.chatforma.com/n8n_node_chatforma)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Segment](actions/add-user-to-segment.md) | `POST /bots/:botId/segments/:segmentId/users` | [docs](https://docs.chatforma.com/) |
| [Create Bot Variable](actions/create-bot-variable.md) | `POST /bots/:botId/variables` | [docs](https://docs.chatforma.com/) |
| [Create Dispatch To Segment](actions/create-dispatch-to-segment.md) | `POST /bots/:botId/segments/:segmentId/dispatch` | [docs](https://docs.chatforma.com/) |
| [Create Dispatch To User](actions/create-dispatch-to-user.md) | `POST /bots/:botId/dispatch/user/:botUserId` | [docs](https://docs.chatforma.com/) |
| [Create User Variable](actions/create-user-variable.md) | `POST /bots/:botId/variables/:variableId/user/:botUserId` | [docs](https://docs.chatforma.com/) |
| [Delete Bot Variable](actions/delete-bot-variable.md) | `DELETE /bots/:botId/variables/:variableId` | [docs](https://docs.chatforma.com/) |
| [Get Current Account](actions/get-current-account.md) | `GET /auth-test` | [docs](https://docs.chatforma.com/) |
| [Get Notification Sample](actions/get-notification-sample.md) | `GET /notification-sample` | [docs](https://docs.chatforma.com/) |
| [Get User Variable](actions/get-user-variable.md) | `GET /bots/:botId/variables/:variableId/user/:botUserId` | [docs](https://docs.chatforma.com/) |
| [List Bot Messages](actions/list-bot-messages.md) | `GET /bots/:botId/messages` | [docs](https://docs.chatforma.com/) |
| [List Bot Users](actions/list-bot-users.md) | `GET /bots/:botId/users` | [docs](https://docs.chatforma.com/) |
| [List Bot Variables](actions/list-bot-variables.md) | `GET /bots/:botId/variables` | [docs](https://docs.chatforma.com/) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://docs.chatforma.com/) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://docs.chatforma.com/) |
| [List Notifications](actions/list-notifications.md) | `GET /notification` | [docs](https://docs.chatforma.com/) |
| [List Open Dialog Users](actions/list-open-dialog-users.md) | `GET /bots/:botId/dialogs/users` | [docs](https://docs.chatforma.com/) |
| [List Segment Users](actions/list-segment-users.md) | `GET /bots/:botId/segments/:segmentId/users` | [docs](https://docs.chatforma.com/) |
| [List Segments](actions/list-segments.md) | `GET /bots/:botId/segments` | [docs](https://docs.chatforma.com/) |
| [List User Messages](actions/list-user-messages.md) | `GET /bots/:botId/dialogs/:userId/messages` | [docs](https://docs.chatforma.com/) |
| [Remove User From Segment](actions/remove-user-from-segment.md) | `DELETE /bots/:botId/segments/:segmentId/users` | [docs](https://docs.chatforma.com/) |
| [Send Existing Message To Segment](actions/send-existing-message-to-segment.md) | `POST /bots/:botId/segments/:segmentId/message/:messageId` | [docs](https://docs.chatforma.com/) |
| [Send Existing Message To User](actions/send-existing-message-to-user.md) | `POST /bots/:botId/user/:botUserId/message/:messageId` | [docs](https://docs.chatforma.com/) |
| [Send Message To Dialog User](actions/send-message-to-dialog-user.md) | `POST /bots/:botId/dialogs/:userId/message` | [docs](https://docs.chatforma.com/) |
| [Subscribe To Notifications](actions/subscribe-to-notifications.md) | `POST /subscribe-notification` | [docs](https://docs.chatforma.com/) |
| [Unsubscribe From Notifications](actions/unsubscribe-from-notifications.md) | `DELETE /unsubscribe-notification` | [docs](https://docs.chatforma.com/) |
