# <img src="https://images.mindcloud.co/apps/icons/sozuri-kenya-sms_1774230891837.png" alt="Sozuri (Kenya) SMS logo" width="28" height="28"> Sozuri (Kenya) SMS: Universal API

Send SMS and WhatsApp messages, manage contacts, and run Sozuri messaging workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sozuriKenyaSMS/latest
- **Category:** Support / Contact Center
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sozuri.net/
- **Vendor API docs:** https://sozuri.net/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contacts](actions/create-contacts.md) | POST | Creates one or more contacts in Sozuri. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Sozuri. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Sozuri. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Sozuri. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Sozuri. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST | Sends bulk SMS messages through Sozuri. |

### Premium Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Premium Ondemand SMS](actions/send-premium-ondemand-sms.md) | POST | Sends an on-demand premium SMS through Sozuri. |
| [Send Premium Subscription SMS](actions/send-premium-subscription-sms.md) | POST | Sends a subscription premium SMS through Sozuri. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Activates a premium SMS subscriber in Sozuri. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deactivates a premium SMS subscriber in Sozuri. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Audio Message](actions/send-whats-app-audio-message.md) | POST | Sends a WhatsApp audio message through Sozuri. |
| [Send WhatsApp Contacts Message](actions/send-whats-app-contacts-message.md) | POST | Sends WhatsApp contact cards through Sozuri. |
| [Send WhatsApp Document Message](actions/send-whats-app-document-message.md) | POST | Sends a WhatsApp document message through Sozuri. |
| [Send WhatsApp Image Message](actions/send-whats-app-image-message.md) | POST | Sends a WhatsApp image message through Sozuri. |
| [Send WhatsApp Interactive List Message](actions/send-whats-app-interactive-list-message.md) | POST | Sends a WhatsApp interactive list through Sozuri. |
| [Send WhatsApp Interactive Reply Buttons Message](actions/send-whats-app-interactive-reply-buttons-message.md) | POST | Sends WhatsApp reply buttons through Sozuri. |
| [Send WhatsApp Location Message](actions/send-whats-app-location-message.md) | POST | Sends a WhatsApp location message through Sozuri. |
| [Send WhatsApp Reaction Message](actions/send-whats-app-reaction-message.md) | POST | Sends a WhatsApp reaction through Sozuri. |
| [Send WhatsApp Reply Text Message](actions/send-whats-app-reply-text-message.md) | POST | Sends a WhatsApp reply text message through Sozuri. |
| [Send WhatsApp Sticker Message](actions/send-whats-app-sticker-message.md) | POST | Sends a WhatsApp sticker message through Sozuri. |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | POST | Sends a WhatsApp text message through Sozuri. |
| [Send WhatsApp Video Message](actions/send-whats-app-video-message.md) | POST | Sends a WhatsApp video message through Sozuri. |

