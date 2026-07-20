# <img src="https://images.mindcloud.co/apps/icons/chat-bot-kit_1774977510131.png" alt="ChatBotKit logo" width="28" height="28"> ChatBotKit: Universal API

Build, manage, and deploy AI agents, datasets, and conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatBotKit/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatbotkit.com
- **Vendor API docs:** https://chatbotkit.com/manuals/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST |  |
| [Delete Bot](actions/delete-bot.md) | DELETE |  |
| [Fetch Bot](actions/fetch-bot.md) | GET |  |
| [List Bots](actions/list-bots.md) | GET |  |
| [Update Bot](actions/update-bot.md) | PUT |  |

### Bot Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Session](actions/create-bot-session.md) | POST |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Ensure Contact Existence](actions/ensure-contact-existence.md) | POST |  |
| [Fetch Contact](actions/fetch-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Complete Conversation Interaction](actions/complete-conversation-interaction.md) | POST |  |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [Fetch Conversation](actions/fetch-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |

### Conversation Completion

| Action | Method | Description |
| --- | --- | --- |
| [Dispatch Stateful Completion](actions/dispatch-stateful-completion.md) | POST |  |

### Conversation Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Message](actions/create-conversation-message.md) | POST |  |
| [Delete Conversation Message](actions/delete-conversation-message.md) | DELETE |  |
| [Fetch Conversation Message](actions/fetch-conversation-message.md) | GET |  |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET |  |
| [Send Conversation Message](actions/send-conversation-message.md) | POST |  |
| [Update Conversation Message](actions/update-conversation-message.md) | PUT |  |

### Conversation Response

| Action | Method | Description |
| --- | --- | --- |
| [Receive AI Response](actions/receive-ai-response.md) | POST |  |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST |  |
| [Delete Dataset](actions/delete-dataset.md) | DELETE |  |
| [List Datasets](actions/list-datasets.md) | GET |  |
| [Retrieve Dataset](actions/retrieve-dataset.md) | GET |  |
| [Update Dataset](actions/update-dataset.md) | PUT |  |

### Dataset Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Record](actions/create-dataset-record.md) | POST |  |
| [Delete Dataset Record](actions/delete-dataset-record.md) | DELETE |  |
| [Fetch Dataset Record](actions/fetch-dataset-record.md) | GET |  |
| [List Dataset Records](actions/list-dataset-records.md) | GET |  |
| [Search Dataset](actions/search-dataset.md) | GET |  |
| [Update Dataset Record](actions/update-dataset-record.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |
| [Retrieve File Details](actions/retrieve-file-details.md) | GET |  |
| [Upload File Content](actions/upload-file-content.md) | PUT |  |

