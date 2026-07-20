# <img src="https://images.mindcloud.co/apps/icons/images-3_1773420786631.png" alt="TimelinesAI logo" width="28" height="28"> TimelinesAI: Universal API

TimelinesAI: Manage WhatsApp chats, messages, files, labels, teammates, and webhooks from a shared inbox and automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timelinesAI/latest
- **Category:** Communication / Team Messaging
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timelines.ai/
- **Vendor API docs:** https://timelinesai.mintlify.app/public-api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List WhatsApp Accounts](actions/list-whatsapp-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat](actions/get-chat.md) | GET | Retrieves details for a TimelinesAI chat. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from your TimelinesAI workspace. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in TimelinesAI. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves details for an uploaded TimelinesAI file. |
| [List Files](actions/list-files.md) | GET | Retrieves uploaded files from your TimelinesAI workspace. |
| [Upload File by Form](actions/upload-file-by-form.md) | POST | Creates a TimelinesAI file from multipart form data. |
| [Upload File by URL](actions/upload-file-by-url.md) | POST | Creates a TimelinesAI file from a public URL. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Add Chat Labels](actions/add-chat-labels.md) | PUT | Adds labels to a specific TimelinesAI chat. |
| [List Chat Labels](actions/list-chat-labels.md) | GET | Retrieves labels for a specific TimelinesAI chat. |
| [Replace Chat Labels](actions/replace-chat-labels.md) | PUT | Replaces all labels on a specific TimelinesAI chat. |

### Message Status Event

| Action | Method | Description |
| --- | --- | --- |
| [List Message Status History](actions/list-message-status-history.md) | GET | Retrieves status history for a TimelinesAI message. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves details for a TimelinesAI message. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from a specific TimelinesAI chat. |
| [Send Chat Message](actions/send-chat-message.md) | POST | Creates a new message in an existing TimelinesAI chat. |
| [Send Message To Chat Name](actions/send-message-to-chat-name.md) | POST | Creates a WhatsApp message in TimelinesAI by chat name. |
| [Send Message to JID](actions/send-message-to-jid.md) | POST | Creates a WhatsApp message in TimelinesAI by JID. |
| [Send Message to Phone](actions/send-message-to-phone.md) | POST | Creates a WhatsApp message in TimelinesAI by phone number. |
| [Send Voice Message To Chat](actions/send-voice-message-to-chat.md) | POST | Creates a voice message in an existing TimelinesAI chat. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Add Chat Note](actions/add-chat-note.md) | POST | Creates a note on an existing TimelinesAI chat. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Reactions](actions/get-message-reactions.md) | GET | Retrieves reactions for a TimelinesAI message. |
| [Update Message Reactions](actions/update-message-reactions.md) | PUT | Updates reactions on an existing TimelinesAI message. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Quotas](actions/get-workspace-quotas.md) | GET | Retrieves workspace quotas and usage from TimelinesAI. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Teammates](actions/list-workspace-teammates.md) | GET | Retrieves teammates from your TimelinesAI workspace. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook subscription in TimelinesAI. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves details for a TimelinesAI webhook subscription. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from your TimelinesAI workspace. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook subscription in TimelinesAI. |

### Whatsapp Account

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Accounts](actions/list-whatsapp-accounts.md) | GET | Retrieves WhatsApp accounts connected in TimelinesAI. |

