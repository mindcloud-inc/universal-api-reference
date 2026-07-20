# <img src="https://images.mindcloud.co/apps/icons/agent-mail_1776453299056.png" alt="Agent Mail logo" width="28" height="28"> Agent Mail: Universal API

Send, receive, and manage agent email workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agentMail/latest
- **Category:** Communication / Email Communications
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agentmail.to
- **Vendor API docs:** https://docs.agentmail.to/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inboxes](actions/list-inboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox Draft Attachment](actions/get-inbox-draft-attachment.md) | GET | Retrieves a draft attachment from a specific AgentMail inbox. |
| [Get Inbox Message Attachment](actions/get-inbox-message-attachment.md) | GET | Retrieves a message attachment from a specific AgentMail inbox. |
| [Get Inbox Thread Attachment](actions/get-inbox-thread-attachment.md) | GET | Retrieves a thread attachment from a specific AgentMail inbox. |

### Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Draft](actions/create-inbox-draft.md) | POST | Creates a new draft in a specific AgentMail inbox. |
| [Delete Inbox Draft](actions/delete-inbox-draft.md) | DELETE | Deletes a draft from a specific AgentMail inbox. |
| [Get Inbox Draft](actions/get-inbox-draft.md) | GET | Retrieves a draft from a specific AgentMail inbox. |
| [List Drafts](actions/list-drafts.md) | GET | Retrieves drafts from AgentMail for the authenticated account. |
| [List Inbox Drafts](actions/list-inbox-drafts.md) | GET | Retrieves drafts from a specific AgentMail inbox. |
| [Send Inbox Draft](actions/send-inbox-draft.md) | POST | Sends a draft from a specific AgentMail inbox. |
| [Update Inbox Draft](actions/update-inbox-draft.md) | PUT | Updates a draft in a specific AgentMail inbox. |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox](actions/create-inbox.md) | POST | Creates a new inbox in AgentMail. |
| [Delete Inbox](actions/delete-inbox.md) | DELETE | Deletes an existing inbox from AgentMail. |
| [Get Inbox](actions/get-inbox.md) | GET | Retrieves a specific inbox from AgentMail. |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves inboxes from AgentMail for the authenticated account. |
| [Update Inbox](actions/update-inbox.md) | PUT | Updates an existing inbox in AgentMail. |

### List Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox List Entry](actions/create-inbox-list-entry.md) | POST | Creates an inbox list entry in a specific AgentMail inbox. |
| [Delete Inbox List Entry](actions/delete-inbox-list-entry.md) | DELETE | Deletes an inbox list entry from a specific AgentMail inbox. |
| [Get Inbox List Entry](actions/get-inbox-list-entry.md) | GET | Retrieves an inbox list entry from a specific AgentMail inbox. |
| [List Inbox List Entries](actions/list-inbox-list-entries.md) | GET | Retrieves inbox list entries from a specific AgentMail inbox. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Inbox Message](actions/delete-inbox-message.md) | DELETE | Permanently deletes a message from a specific AgentMail inbox. |
| [Forward Inbox Message](actions/forward-inbox-message.md) | POST | Forwards a message from a specific AgentMail inbox. |
| [Get Inbox Message](actions/get-inbox-message.md) | GET | Retrieves a message from a specific AgentMail inbox. |
| [List Inbox Messages](actions/list-inbox-messages.md) | GET | Retrieves messages from a specific AgentMail inbox. |
| [Reply All To Inbox Message](actions/reply-all-to-inbox-message.md) | POST | Replies to all recipients of an AgentMail message. |
| [Reply To Inbox Message](actions/reply-to-inbox-message.md) | POST | Replies to a message from a specific AgentMail inbox. |
| [Send Inbox Message](actions/send-inbox-message.md) | POST | Sends a new message from a specific AgentMail inbox. |
| [Update Inbox Message](actions/update-inbox-message.md) | PUT | Updates a message in a specific AgentMail inbox. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves the authenticated organization details from AgentMail. |

### Raw Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Raw Inbox Message](actions/get-raw-inbox-message.md) | GET | Retrieves the raw message from a specific AgentMail inbox. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Delete Inbox Thread](actions/delete-inbox-thread.md) | DELETE | Deletes a thread from AgentMail, or permanently deletes trashed threads. |
| [Get Inbox Thread](actions/get-inbox-thread.md) | GET | Retrieves a thread from a specific AgentMail inbox. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a specific thread from AgentMail. |
| [List Inbox Threads](actions/list-inbox-threads.md) | GET | Retrieves threads from a specific AgentMail inbox. |
| [List Threads](actions/list-threads.md) | GET | Retrieves threads from AgentMail for the authenticated account. |
| [Update Inbox Thread](actions/update-inbox-thread.md) | PUT | Updates a thread in a specific AgentMail inbox. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in AgentMail. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from AgentMail. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a specific webhook from AgentMail. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from AgentMail for the authenticated account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in AgentMail. |

