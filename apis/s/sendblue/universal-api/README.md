# <img src="https://images.mindcloud.co/apps/icons/sendblue_1773434055828.png" alt="Sendblue logo" width="28" height="28"> Sendblue: Universal API

Send messages, manage contacts, and receive webhooks with Sendblue

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendblue/latest
- **Category:** Communication / Team Messaging
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sendblue.com
- **Vendor API docs:** https://docs.sendblue.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact?connectionId=$CONNECTION_ID&phoneNumber=%2B14155550123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Sendblue. |
| [Create Multiple Contacts](actions/create-multiple-contacts.md) | POST | Creates multiple contacts in Sendblue. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Sendblue. |
| [Delete Multiple Contacts](actions/delete-multiple-contacts.md) | DELETE | Deletes multiple contacts from Sendblue. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Sendblue by phone number. |
| [Get Contact Count](actions/get-contact-count.md) | GET | Retrieves the contact count from Sendblue. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Sendblue. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Sendblue. |
| [Verify Contact](actions/verify-contact.md) | POST | Sends a verification message to a contact in Sendblue. |

### Group Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Group Message](actions/send-group-message.md) | POST | Sends a group message through Sendblue. |

### Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Phone Number](actions/lookup-phone-number.md) | GET | Determines whether a phone number supports iMessage or SMS. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Direct File Upload](actions/direct-file-upload.md) | POST | Uploads a file to Sendblue for iMessage attachments. |
| [Upload Media Object](actions/upload-media-object.md) | POST | Uploads a media object to Sendblue. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Soft deletes a message from Sendblue. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Sendblue by ID. |
| [Get Message Status](actions/get-message-status.md) | GET | Retrieves the status of a message from Sendblue. |
| [List Messages](actions/list-messages.md) | GET | Retrieves a list of messages from Sendblue. |
| [Send Message](actions/send-message.md) | POST | Sends a message through Sendblue. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Send Reaction](actions/send-reaction.md) | POST | Sends an iMessage reaction through Sendblue. |

### Read Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Send Read Receipt](actions/send-read-receipt.md) | POST | Sends a read receipt through Sendblue. |

### Typing Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Send Typing Indicator](actions/send-typing-indicator.md) | POST | Sends an iMessage typing indicator through Sendblue. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhooks](actions/add-webhooks.md) | POST | Adds webhooks to Sendblue. |
| [Delete Webhooks](actions/delete-webhooks.md) | DELETE | Deletes webhooks from Sendblue. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Sendblue. |
| [Replace Webhooks](actions/replace-webhooks.md) | PUT | Replaces webhooks in Sendblue. |

