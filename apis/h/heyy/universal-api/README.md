# <img src="https://images.mindcloud.co/apps/icons/691a49c3e6f5e0ff6c8d57a8-logo-small-11_1775043660820.png" alt="Heyy logo" width="28" height="28"> Heyy: Universal API

Heyy lets teams manage WhatsApp conversations, contacts, broadcasts, automations, labels, files, webhooks, and workspace configuration through the Heyy API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/heyy/latest
- **Category:** Communication / Team Messaging
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.heyy.io
- **Vendor API docs:** https://docs.heyy.io/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Business](actions/get-business.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-business?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Api Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create API Webhook](actions/create-api-webhook.md) | POST | Creates a new API webhook in Heyy. |
| [Delete API Webhook](actions/delete-api-webhook.md) | DELETE | Deletes an existing API webhook from Heyy. |
| [List API Webhooks](actions/list-api-webhooks.md) | GET | Retrieves API webhooks from a Heyy workspace. |
| [Update API Webhook](actions/update-api-webhook.md) | PUT | Updates an existing API webhook in Heyy. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Attribute](actions/create-attribute.md) | POST | Creates a new attribute in Heyy. |
| [Delete Attribute](actions/delete-attribute.md) | DELETE | Deletes an existing attribute from Heyy. |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves attributes from a Heyy workspace. |

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from a Heyy channel. |
| [Trigger Automation](actions/trigger-automation.md) | POST | Triggers an automation in a Heyy channel. |

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Create Broadcast](actions/create-broadcast.md) | POST | Creates a new broadcast in a Heyy channel. |
| [Delete Broadcast](actions/delete-broadcast.md) | DELETE | Deletes an existing broadcast from a Heyy channel. |
| [Get Broadcast by ID](actions/get-broadcast-by-id.md) | GET | Retrieves a broadcast by ID from Heyy. |
| [List Broadcasts](actions/list-broadcasts.md) | GET | Retrieves broadcasts from a Heyy channel. |
| [Start Broadcast](actions/start-broadcast.md) | PUT | Starts a broadcast in a Heyy channel. |
| [Update Broadcast](actions/update-broadcast.md) | PUT | Updates an existing broadcast in a Heyy channel. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel by ID](actions/get-channel-by-id.md) | GET | Retrieves a channel by ID from Heyy. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from a Heyy workspace. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat by ID](actions/get-chat-by-id.md) | GET | Retrieves a chat by ID from Heyy. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from a Heyy channel. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in a Heyy channel. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Attribute](actions/add-contact-attribute.md) | PUT | Adds an attribute to a contact in Heyy. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Heyy. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Heyy. |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET | Retrieves a contact by ID from Heyy. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Heyy workspace. |
| [Remove Contact Attribute](actions/remove-contact-attribute.md) | PUT | Removes an attribute from a contact in Heyy. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Heyy. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to a Heyy workspace. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Heyy. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from Heyy. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from a Heyy workspace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | POST | Sends a WhatsApp message from a Heyy channel. |

### Message Template

| Action | Method | Description |
| --- | --- | --- |
| [List Message Templates](actions/list-message-templates.md) | GET | Retrieves message templates from a Heyy workspace. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Add Recipients To Broadcast](actions/add-recipients-to-broadcast.md) | PUT | Adds recipients to a broadcast in Heyy. |
| [List Broadcast Recipients](actions/list-broadcast-recipients.md) | GET | Retrieves broadcast recipients from a Heyy channel. |
| [Remove Recipients From Broadcast](actions/remove-recipients-from-broadcast.md) | PUT | Removes recipients from a broadcast in Heyy. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Business](actions/get-business.md) | GET | Retrieves business details for a Heyy workspace. |

