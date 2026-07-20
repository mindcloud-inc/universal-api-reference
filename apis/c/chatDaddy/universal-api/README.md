# <img src="https://images.mindcloud.co/apps/icons/images-5_1774368845254.jpeg" alt="ChatDaddy logo" width="28" height="28"> ChatDaddy: Universal API

Manage ChatDaddy contacts, messages, and WhatsApp account operations through the live Instant Messaging API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatDaddy/latest
- **Category:** Communication / Team Messaging
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatdaddy.tech
- **Vendor API docs:** https://chatdaddy.stoplight.io/docs/openapi/7492869297330-getting-started-with-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Boards](actions/list-crm-boards.md) | GET | Retrieves CRM board records from ChatDaddy. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Close Account Connection](actions/close-account-connection.md) | PUT | Closes a connection to a ChatDaddy account. |
| [Create Account](actions/create-account.md) | POST | Creates a new account in ChatDaddy. |
| [Delete Account](actions/delete-account.md) | DELETE | Enqueues deletion of an account in ChatDaddy. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves connected account records from ChatDaddy. |
| [Open Account Connection](actions/open-account-connection.md) | PUT | Opens a connection to a ChatDaddy account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Check Contact Exists](actions/check-contact-exists.md) | GET | Checks whether a contact exists in ChatDaddy. |
| [Create Contacts](actions/create-contacts.md) | POST | Creates or updates contacts in ChatDaddy. |
| [Delete Contacts](actions/delete-contacts.md) | DELETE | Deletes one or more existing contacts from ChatDaddy. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from your ChatDaddy account. |
| [Update Contacts](actions/update-contacts.md) | PUT | Updates one or more existing contacts in ChatDaddy. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Chats](actions/list-chats.md) | GET | Retrieves chat records from your ChatDaddy account. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in ChatDaddy. |
| [Update Chat Presence](actions/update-chat-presence.md) | PUT | Updates a chat's presence in ChatDaddy. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in ChatDaddy. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from ChatDaddy. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tag records from your ChatDaddy account. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in ChatDaddy. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from ChatDaddy. |
| [Get Bulk Messages](actions/get-bulk-messages.md) | GET | Retrieves bulk message records from ChatDaddy. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from a chat in ChatDaddy. |
| [Search Messages](actions/search-messages.md) | GET | Finds message records in your ChatDaddy account. |
| [Send Message](actions/send-message.md) | POST | Sends a message to a ChatDaddy chat. |
| [Send Message to Chats](actions/send-message-to-chats.md) | POST | Sends a message to one or more ChatDaddy chats. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message or note in ChatDaddy. |
| [Update Messages in Bulk](actions/update-messages-in-bulk.md) | PUT | Performs bulk actions on messages in ChatDaddy. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Ticket](actions/create-crm-ticket.md) | POST | Creates a new CRM ticket in ChatDaddy. |
| [Delete CRM Ticket](actions/delete-crm-ticket.md) | DELETE | Deletes an existing CRM ticket from ChatDaddy. |
| [List CRM Tickets](actions/list-crm-tickets.md) | GET | Retrieves CRM ticket records from ChatDaddy. |
| [Update CRM Ticket](actions/update-crm-ticket.md) | PUT | Updates an existing CRM ticket in ChatDaddy. |

