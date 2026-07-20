# <img src="https://images.mindcloud.co/apps/icons/icon0_1775064684873.png" alt="SparrowDesk logo" width="28" height="28"> SparrowDesk: Universal API

SparrowDesk helpdesk REST API for contacts, conversations, members, tags, and conversation-field management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sparrowDesk/latest
- **Category:** Support / Contact Center
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sparrowdesk.com
- **Vendor API docs:** https://developer.sparrowdesk.com/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from SparrowDesk. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in SparrowDesk. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from SparrowDesk. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from SparrowDesk. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in SparrowDesk. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a conversation in SparrowDesk. |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes an existing conversation from SparrowDesk. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from SparrowDesk. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from SparrowDesk. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in SparrowDesk. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Field](actions/create-conversation-field.md) | POST | Creates a conversation field in SparrowDesk. |
| [Get Conversation Field](actions/get-conversation-field.md) | GET | Retrieves a conversation field from SparrowDesk. |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves contact fields from SparrowDesk. |
| [List Conversation Fields](actions/list-conversation-fields.md) | GET | Retrieves conversation fields from SparrowDesk. |
| [Update Conversation Field](actions/update-conversation-field.md) | PUT | Updates an existing conversation field in SparrowDesk. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | POST | Creates contacts in bulk in SparrowDesk. |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | GET | Retrieves bulk job status from SparrowDesk. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Reply](actions/add-conversation-reply.md) | POST | Creates a conversation reply in SparrowDesk. |
| [List Conversation Replies](actions/list-conversation-replies.md) | GET | Retrieves conversation replies from SparrowDesk. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from SparrowDesk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves members from SparrowDesk. |

