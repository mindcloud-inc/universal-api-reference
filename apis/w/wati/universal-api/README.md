# <img src="https://images.mindcloud.co/apps/icons/wati_1773257278318.png" alt="Wati logo" width="28" height="28"> Wati: Universal API

Manage WhatsApp messages, contacts, and message templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wati/latest
- **Category:** Communication / Team Messaging
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wati.io
- **Vendor API docs:** https://docs.wati.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Message Templates](actions/list-message-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Send Template Messages](actions/send-template-messages.md) | POST | Sends template messages to multiple contacts in Wati. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Wati. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Wati using optional filters. |
| [Update Contact Attributes](actions/update-contact-attributes.md) | PUT | Updates contact attributes for one contact in Wati. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Assign User](actions/assign-user.md) | PUT | Updates a conversation assignment in Wati. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Get Media by File Name](actions/get-media-by-file-name.md) | GET | Retrieves a media file from Wati by file name. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages by WhatsApp Number](actions/list-messages-by-whatsapp-number.md) | GET | Retrieves message history for a WhatsApp number from Wati. |
| [Send File to Open Session](actions/send-file-to-open-session.md) | POST | Sends a file in an open Wati session. |
| [Send Interactive Buttons Message](actions/send-interactive-buttons-message.md) | POST | Sends an interactive button message in Wati. |
| [Send Interactive List Message](actions/send-interactive-list-message.md) | POST | Sends an interactive list message in Wati. |
| [Send Message to Open Session](actions/send-message-to-open-session.md) | POST | Sends a text message in an open Wati session. |
| [Send Template Message](actions/send-template-message.md) | POST | Sends an approved WhatsApp template message through Wati. |

### Message Template

| Action | Method | Description |
| --- | --- | --- |
| [List Message Templates](actions/list-message-templates.md) | GET | Retrieves available message templates from Wati. |

### Message Template Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Send Template Messages CSV](actions/send-template-messages-csv.md) | POST | Sends template messages from a CSV file in Wati. |

