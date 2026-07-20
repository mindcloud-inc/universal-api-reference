# <img src="https://images.mindcloud.co/apps/icons/reply-cx_1775665196621.png" alt="ReplyCX logo" width="28" height="28"> ReplyCX: Universal API

Manage live chat, bots, tickets, and omnichannel customer conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/replyCX/latest
- **Category:** Support / Ticketing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reply.cx
- **Vendor API docs:** https://help.reply.cx/integrations/public-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Change Conversation Assignee](actions/change-conversation-assignee.md) | PUT |  |
| [Close Conversation](actions/close-conversation.md) | PUT |  |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Update Conversation Variables](actions/update-conversation-variables.md) | PUT |  |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Source Training Status](actions/get-data-source-training-status.md) | GET |  |

### Knowledge Base Source

| Action | Method | Description |
| --- | --- | --- |
| [Upload Knowledge Base File Source](actions/upload-knowledge-base-file-source.md) | POST |  |
| [Upload Knowledge Base Text Source](actions/upload-knowledge-base-text-source.md) | POST |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send File Reply To Conversation](actions/send-file-reply-to-conversation.md) | POST |  |
| [Send Template Reply To Conversation](actions/send-template-reply-to-conversation.md) | POST |  |
| [Send Text Reply To Conversation](actions/send-text-reply-to-conversation.md) | POST |  |
| [Send Voice Reply To Conversation](actions/send-voice-reply-to-conversation.md) | POST |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Set Events Webhook](actions/set-events-webhook.md) | PUT |  |

