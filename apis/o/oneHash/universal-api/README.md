# <img src="https://images.mindcloud.co/apps/icons/onehash-icon-square_1775163745516.png" alt="OneHash logo" width="28" height="28"> OneHash: Universal API

OneHash Chat is a customer support workspace built on the Chatwoot API contract. This app wraps the authenticated account-scoped API for contacts, conversations, inboxes, teams, labels, canned responses, webhooks, and related support operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneHash/latest
- **Category:** Support / Ticketing
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onehash.ai
- **Vendor API docs:** https://developers.chatwoot.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from OneHash. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in OneHash. |
| [Create Contact Inbox](actions/create-contact-inbox.md) | POST | Creates a contact inbox in OneHash. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from OneHash. |
| [Filter Contacts](actions/filter-contacts.md) | GET | Finds contacts in OneHash using filters. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from OneHash. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from OneHash. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in OneHash by email address. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in OneHash. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Assign Conversation](actions/assign-conversation.md) | PUT | Updates a conversation assignment in OneHash. |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in OneHash. |
| [Filter Conversations](actions/filter-conversations.md) | GET | Finds conversations in OneHash using filters. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from OneHash. |
| [Get Conversation Counts](actions/get-conversation-counts.md) | GET | Retrieves conversation counts from OneHash. |
| [List Contact Conversations](actions/list-contact-conversations.md) | GET | Retrieves a contact's conversations from OneHash. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from OneHash. |
| [Toggle Conversation Priority](actions/toggle-conversation-priority.md) | PUT | Updates conversation priority in OneHash. |
| [Toggle Conversation Status](actions/toggle-conversation-status.md) | PUT | Updates conversation status in OneHash. |
| [Toggle Conversation Typing Status](actions/toggle-conversation-typing-status.md) | PUT | Updates conversation typing status in OneHash. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in OneHash. |
| [Update Conversation Custom Attributes](actions/update-conversation-custom-attributes.md) | PUT | Updates conversation custom attributes in OneHash. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Reporting Events](actions/get-conversation-reporting-events.md) | GET | Retrieves conversation reporting events from OneHash. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Labels](actions/add-contact-labels.md) | PUT | Updates a contact's labels in OneHash. |
| [Add Conversation Labels](actions/add-conversation-labels.md) | PUT | Updates a conversation's labels in OneHash. |
| [Create Label](actions/create-label.md) | POST | Creates a new label in OneHash. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from OneHash. |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from OneHash. |
| [List Contact Labels](actions/list-contact-labels.md) | GET | Retrieves a contact's labels from OneHash. |
| [List Conversation Labels](actions/list-conversation-labels.md) | GET | Retrieves a conversation's labels from OneHash. |
| [List Labels](actions/list-labels.md) | GET | Retrieves account labels from OneHash. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in OneHash. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Canned Response](actions/create-canned-response.md) | POST | Creates a new canned response in OneHash. |
| [Create Conversation Message](actions/create-conversation-message.md) | POST | Creates a new conversation message in OneHash. |
| [Delete Canned Response](actions/delete-canned-response.md) | DELETE | Deletes an existing canned response from OneHash. |
| [List Canned Responses](actions/list-canned-responses.md) | GET | Retrieves canned responses from OneHash. |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves conversation messages from OneHash. |
| [Update Canned Response](actions/update-canned-response.md) | PUT | Updates an existing canned response in OneHash. |

