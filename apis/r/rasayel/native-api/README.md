# Rasayel: Native API Reference

A consolidated summary of Rasayel's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.rasayel.io/introduction/welcome
- **API base URL:** `https://api.rasayel.io/api/graphql`

## Authentication

### Basic Auth

Use the Rasayel API Key ID as the username and API Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.rasayel.io/graphql/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Conversation](actions/assign-conversation.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Assign Conversation Team](actions/assign-conversation-team.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Attachment Image Upload From URL](actions/attachment-image-upload-from-url.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Attachment Upload From URL](actions/attachment-upload-from-url.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Attachment Video Upload From URL](actions/attachment-video-upload-from-url.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Channel User](actions/create-channel-user.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create GIF Message](actions/create-gif-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Media Message](actions/create-media-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Note Message](actions/create-note-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Proactive Text Message](actions/create-proactive-text-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Rich Message](actions/create-rich-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Template Message](actions/create-template-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Create Text Message](actions/create-text-message.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Get App](actions/get-app.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [GraphQL Query](actions/graph-ql-query.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Set Conversation State](actions/set-conversation-state.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Snooze Conversation](actions/snooze-conversation.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Tag Channel User](actions/tag-channel-user.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Tag Channel User By Tag ID](actions/tag-channel-user-by-tag-id.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Tag Conversation](actions/tag-conversation.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Tag Conversation By Tag ID](actions/tag-conversation-by-tag-id.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Unsnooze Conversation](actions/unsnooze-conversation.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Untag Channel User](actions/untag-channel-user.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Untag Conversation](actions/untag-conversation.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User](actions/update-channel-user.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Bool Attribute](actions/update-channel-user-bool-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Date Attribute](actions/update-channel-user-date-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Decimal Attribute](actions/update-channel-user-decimal-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Identifier](actions/update-channel-user-identifier.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Number Attribute](actions/update-channel-user-number-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Select Attribute](actions/update-channel-user-select-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
| [Update Channel User Text Attribute](actions/update-channel-user-text-attribute.md) | `POST /` | [docs](https://developers.rasayel.io/graphql/api) |
