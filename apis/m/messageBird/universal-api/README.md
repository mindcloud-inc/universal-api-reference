# <img src="https://images.mindcloud.co/apps/icons/message-bird_1774035424416.png" alt="MessageBird logo" width="28" height="28"> MessageBird: Universal API

Manage Bird conversations, channels, and customer messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/messageBird/latest
- **Category:** Communication / Team Messaging
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bird.com
- **Vendor API docs:** https://docs.bird.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspace Channels](actions/list-workspace-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-workspace-channels?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET |  |
| [Get Channel Details for a Contact](actions/get-channel-details-for-a-contact.md) | GET |  |
| [Get Conversations Configuration](actions/get-conversations-configuration.md) | GET |  |
| [List Workspace Channels](actions/list-workspace-channels.md) | GET |  |
| [Update Conversations Configuration](actions/update-conversations-configuration.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [List Participant Conversations](actions/list-participant-conversations.md) | GET |  |
| [List Participant Conversations by Identifier](actions/list-participant-conversations-by-identifier.md) | GET |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Participant](actions/add-conversation-participant.md) | POST |  |
| [Create Navigator](actions/create-navigator.md) | POST |  |
| [Delete Conversation Participant](actions/delete-conversation-participant.md) | DELETE |  |
| [Delete Navigator](actions/delete-navigator.md) | DELETE |  |
| [Get Conversation Participant](actions/get-conversation-participant.md) | GET |  |
| [Get Conversation Participant by Identifier](actions/get-conversation-participant-by-identifier.md) | GET |  |
| [Get Navigator](actions/get-navigator.md) | GET |  |
| [Get Navigator Coverage](actions/get-navigator-coverage.md) | GET |  |
| [List Conversation Participants](actions/list-conversation-participants.md) | GET |  |
| [List Navigators](actions/list-navigators.md) | GET |  |
| [Update Conversation Participant](actions/update-conversation-participant.md) | PUT |  |
| [Update Conversation Participant by Identifier](actions/update-conversation-participant-by-identifier.md) | PUT |  |
| [Update Navigator](actions/update-navigator.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Message](actions/create-conversation-message.md) | POST |  |
| [Create Pre-Signed Upload](actions/create-pre-signed-upload.md) | POST |  |
| [Delete Conversation Message](actions/delete-conversation-message.md) | DELETE |  |
| [Get Channel Message](actions/get-channel-message.md) | GET |  |
| [Get Conversation Message](actions/get-conversation-message.md) | GET |  |
| [List Channel Messages](actions/list-channel-messages.md) | GET |  |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET |  |
| [List Message Interactions](actions/list-message-interactions.md) | GET |  |
| [List Workspace Messages](actions/list-workspace-messages.md) | GET |  |
| [Send Navigator Message](actions/send-navigator-message.md) | POST |  |
| [Update Conversation Message](actions/update-conversation-message.md) | PUT |  |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Add Allow/Block Rules in Bulk](actions/add-allowblock-rules-in-bulk.md) | POST |  |
| [Create Allow/Block Rule](actions/create-allowblock-rule.md) | POST |  |
| [Delete Allow/Block Rule](actions/delete-allowblock-rule.md) | DELETE |  |
| [Get Allow/Block Bulk Upload Status](actions/get-allowblock-bulk-upload-status.md) | GET |  |
| [Get Allow/Block Rule](actions/get-allowblock-rule.md) | GET |  |
| [List Allow/Block Rules](actions/list-allowblock-rules.md) | GET |  |
| [Update Allow/Block Rule](actions/update-allowblock-rule.md) | PUT |  |
| [Update Antispam Setting](actions/update-antispam-setting.md) | PUT |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

