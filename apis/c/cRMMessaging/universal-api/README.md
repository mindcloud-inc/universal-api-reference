# <img src="https://images.mindcloud.co/apps/icons/light-blue_1774298995829.jpeg" alt="CRM Messaging logo" width="28" height="28"> CRM Messaging: Universal API

Send SMS, WhatsApp, voice calls, and manage contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cRMMessaging/latest
- **Category:** Communication / Team Messaging
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crm-messaging.cloud
- **Vendor API docs:** https://crm-messaging.cloud/docs-category/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Make Voice Call](actions/make-voice-call.md) | POST | Starts a voice call in CRM Messaging. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in CRM Messaging. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from CRM Messaging. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in CRM Messaging. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from CRM Messaging. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS from CRM Messaging. |
| [Send WhatsApp Template](actions/send-whats-app-template.md) | POST | Sends a WhatsApp template from CRM Messaging. |

