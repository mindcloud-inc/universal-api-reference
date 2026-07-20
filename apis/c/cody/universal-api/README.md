# <img src="https://images.mindcloud.co/apps/icons/group-1_1781294654070.png" alt="Cody logo" width="28" height="28"> Cody: Universal API

Cody is an AI-powered knowledge base for employees that lets you manage bots, conversations, documents, folders, messages, and uploads through the Cody API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cody/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getcody.ai/
- **Vendor API docs:** https://developers.meetcody.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Conversation](actions/get-conversation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cody/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Create Document from File](actions/create-document-from-file.md) | POST |  |
| [Create Document from Webpage](actions/create-document-from-webpage.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |
| [Send Message](actions/send-message.md) | POST |  |

### Message Stream

| Action | Method | Description |
| --- | --- | --- |
| [Send Message for Stream](actions/send-message-for-stream.md) | POST |  |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload URL](actions/get-upload-url.md) | POST |  |

