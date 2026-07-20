# <img src="https://images.mindcloud.co/apps/icons/smart-sender_1775660226869.png" alt="Smart Sender logo" width="28" height="28"> Smart Sender: Universal API

Manage chats, contacts, channels, messages, variables, funnels, tags, and products in Smart Sender

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartSender/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smartsender.com
- **Vendor API docs:** https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1705902128/API-kuvaus

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Smart Sender. |
| [List Channels](actions/list-channels.md) | GET | Retrieves project channels from Smart Sender. |
| [Update Channel](actions/update-channel.md) | PUT | Updates a channel's activity status in Smart Sender. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Assign Chat](actions/assign-chat.md) | PUT | Assigns a chat to an operator in Smart Sender. |
| [Close Chat](actions/close-chat.md) | PUT | Closes a chat in Smart Sender. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Smart Sender. |
| [Get Contact Chat](actions/get-contact-chat.md) | GET | Retrieves a contact's chat from Smart Sender. |
| [List Chats](actions/list-chats.md) | GET | Retrieves project chats from Smart Sender. |
| [Mark Chat Read](actions/mark-chat-read.md) | PUT | Marks a chat as read in Smart Sender. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Smart Sender. |
| [Get Contact Info](actions/get-contact-info.md) | GET | Retrieves simplified contact details from Smart Sender. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves project contacts from Smart Sender. |
| [Merge Contacts](actions/merge-contacts.md) | PUT | Merges one contact into another in Smart Sender. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Smart Sender by keyword. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Smart Sender. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Fire Contact Event](actions/fire-contact-event.md) | POST | Triggers an event for a contact in Smart Sender. |

### Funnel

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Funnel](actions/add-contact-funnel.md) | POST | Adds a funnel subscription to a contact in Smart Sender. |
| [List Contact Funnels](actions/list-contact-funnels.md) | GET | Retrieves funnel subscriptions for a contact in Smart Sender. |
| [Remove Contact Funnel](actions/remove-contact-funnel.md) | DELETE | Removes a funnel subscription from a contact in Smart Sender. |

### Gate

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel Gate](actions/create-channel-gate.md) | POST | Creates a channel gateway in Smart Sender, or returns the existing one. |
| [Get Contact Gates](actions/get-contact-gates.md) | GET | Retrieves a contact's available communication channels from Smart Sender. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages for a chat in Smart Sender. |
| [List Contact Messages](actions/list-contact-messages.md) | GET | Retrieves messages for a contact in Smart Sender. |
| [Send Message](actions/send-message.md) | POST | Sends a message to a contact in Smart Sender. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Smart Sender. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Smart Sender. |
| [List Products](actions/list-products.md) | GET | Retrieves project products from Smart Sender. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Smart Sender. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tag](actions/add-contact-tag.md) | POST | Adds a tag to a contact in Smart Sender. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves tags for a contact in Smart Sender. |
| [Remove Contact Tag](actions/remove-contact-tag.md) | DELETE | Removes a tag from a contact in Smart Sender. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Variable](actions/create-variable.md) | POST | Creates a new variable in Smart Sender. |
| [Delete Variable](actions/delete-variable.md) | DELETE | Deletes an existing variable from Smart Sender. |
| [List Variables](actions/list-variables.md) | GET | Retrieves project variables from Smart Sender. |
| [Update Variable](actions/update-variable.md) | PUT | Updates an existing variable in Smart Sender. |

