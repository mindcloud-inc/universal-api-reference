# <img src="https://images.mindcloud.co/apps/icons/intercom-logo-black-and-white-2_1773337075274.png" alt="Intercom logo" width="28" height="28"> Intercom: Universal API

Manage contacts, conversations, tickets, and customer messaging

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intercom/latest
- **Category:** Support / Ticketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.intercom.com
- **Vendor API docs:** https://developers.intercom.com/docs/references/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Archive Contact](actions/archive-contact.md) | PUT |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Get Contact By External ID](actions/get-contact-by-external-id.md) | GET |  |
| [List Contact Companies](actions/list-contact-companies.md) | GET |  |
| [List Contact Segments](actions/list-contact-segments.md) | GET |  |
| [List Contact Subscriptions](actions/list-contact-subscriptions.md) | GET |  |
| [List Contact Tags](actions/list-contact-tags.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Merge Contact](actions/merge-contact.md) | PUT |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Unarchive Contact](actions/unarchive-contact.md) | PUT |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Attach Contact To Conversation](actions/attach-contact-to-conversation.md) | PUT |  |
| [Convert Conversation To Ticket](actions/convert-conversation-to-ticket.md) | PUT |  |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Manage Conversation Part](actions/manage-conversation.md) | PUT |  |
| [Redact Conversation](actions/redact-conversation.md) | PUT |  |
| [Reply Conversation](actions/reply-conversation.md) | PUT |  |
| [Retrieve Conversation](actions/retrieve-conversation.md) | GET |  |
| [Search Conversations](actions/search-conversations.md) | GET |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Delete Ticket](actions/delete-ticket.md) | DELETE |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [Reply Ticket](actions/reply-ticket.md) | PUT |  |
| [Search Tickets](actions/search-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

