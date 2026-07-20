# <img src="https://images.mindcloud.co/apps/icons/rasayel_1775824558395.png" alt="Rasayel logo" width="28" height="28"> Rasayel: Universal API

Manage conversations, contacts, campaigns, and messaging in Rasayel

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rasayel/latest
- **Category:** Communication / Team Messaging
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.rasayel.io
- **Vendor API docs:** https://developers.rasayel.io/introduction/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App](actions/get-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Attachment Image Upload From URL](actions/attachment-image-upload-from-url.md) | POST | Creates an image attachment in Rasayel from a URL. |
| [Attachment Upload From URL](actions/attachment-upload-from-url.md) | POST | Creates an attachment in Rasayel from a URL. |
| [Attachment Video Upload From URL](actions/attachment-video-upload-from-url.md) | POST | Creates a video attachment in Rasayel from a URL. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel User](actions/create-channel-user.md) | POST | Creates a new channel user in Rasayel. |
| [Tag Channel User](actions/tag-channel-user.md) | PUT | Adds a tag to a channel user in Rasayel. |
| [Tag Channel User By Tag ID](actions/tag-channel-user-by-tag-id.md) | PUT | Adds a tag to a Rasayel channel user by tag ID. |
| [Untag Channel User](actions/untag-channel-user.md) | PUT | Removes a tag from a channel user in Rasayel. |
| [Update Channel User](actions/update-channel-user.md) | PUT | Updates an existing channel user in Rasayel. |
| [Update Channel User Bool Attribute](actions/update-channel-user-bool-attribute.md) | PUT | Updates a boolean attribute on a Rasayel channel user. |
| [Update Channel User Date Attribute](actions/update-channel-user-date-attribute.md) | PUT | Updates a date attribute on a Rasayel channel user. |
| [Update Channel User Decimal Attribute](actions/update-channel-user-decimal-attribute.md) | PUT | Updates a decimal attribute on a Rasayel channel user. |
| [Update Channel User Identifier](actions/update-channel-user-identifier.md) | PUT | Updates a Rasayel channel user's identifier. |
| [Update Channel User Number Attribute](actions/update-channel-user-number-attribute.md) | PUT | Updates a number attribute on a Rasayel channel user. |
| [Update Channel User Select Attribute](actions/update-channel-user-select-attribute.md) | PUT | Updates a select attribute on a Rasayel channel user. |
| [Update Channel User Text Attribute](actions/update-channel-user-text-attribute.md) | PUT | Updates a text attribute on a Rasayel channel user. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Assign Conversation](actions/assign-conversation.md) | PUT | Assigns a conversation to a user in Rasayel. |
| [Assign Conversation Team](actions/assign-conversation-team.md) | PUT | Assigns a conversation to a team in Rasayel. |
| [Set Conversation State](actions/set-conversation-state.md) | PUT | Updates a conversation's state in Rasayel. |
| [Snooze Conversation](actions/snooze-conversation.md) | PUT | Snoozes an existing conversation in Rasayel. |
| [Tag Conversation](actions/tag-conversation.md) | PUT | Adds a tag to a conversation in Rasayel. |
| [Tag Conversation By Tag ID](actions/tag-conversation-by-tag-id.md) | PUT | Adds a tag to a Rasayel conversation by tag ID. |
| [Unsnooze Conversation](actions/unsnooze-conversation.md) | PUT | Unsnoozes an existing conversation in Rasayel. |
| [Untag Conversation](actions/untag-conversation.md) | PUT | Removes a tag from a conversation in Rasayel. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create GIF Message](actions/create-gif-message.md) | POST | Creates a GIF message in Rasayel. |
| [Create Media Message](actions/create-media-message.md) | POST | Creates a media message in Rasayel. |
| [Create Note Message](actions/create-note-message.md) | POST | Creates a note message in Rasayel. |
| [Create Proactive Text Message](actions/create-proactive-text-message.md) | POST | Creates a proactive text message in Rasayel. |
| [Create Rich Message](actions/create-rich-message.md) | POST | Creates a rich message in Rasayel. |
| [Create Template Message](actions/create-template-message.md) | POST | Creates a template message in Rasayel. |
| [Create Text Message](actions/create-text-message.md) | POST | Creates a text message in Rasayel. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [GraphQL Query](actions/graph-ql-query.md) | GET | Makes an authenticated raw GraphQL request to Rasayel. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves the current Rasayel workspace details. |

