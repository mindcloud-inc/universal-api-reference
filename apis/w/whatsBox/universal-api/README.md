# <img src="https://images.mindcloud.co/apps/icons/whats-box_1774907537973.png" alt="WhatsBox logo" width="28" height="28"> WhatsBox: Universal API

Manage WhatsApp conversations, broadcasts, templates, contacts, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whatsBox/latest
- **Category:** Communication / Team Messaging
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.whatsbox.io
- **Vendor API docs:** https://api.whatsbox.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Organization](actions/get-my-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-my-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves connected WhatsApp phone numbers from WhatsBox. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in WhatsBox. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from WhatsBox. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from WhatsBox. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves all contact lists from WhatsBox. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in WhatsBox. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Media Message](actions/send-media-message.md) | POST | Sends a media message from WhatsBox within the 24-hour window. |
| [Send Template Message](actions/send-template-message.md) | POST | Sends an approved template message from WhatsBox. |
| [Send Text Message](actions/send-text-message.md) | POST | Sends a text message from WhatsBox within the 24-hour window. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get My Organization](actions/get-my-organization.md) | GET | Retrieves your organization details from WhatsBox. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Check Service Health](actions/check-service-health.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a WhatsApp template from WhatsBox. |
| [List Templates](actions/list-templates.md) | GET | Retrieves all message templates from WhatsBox. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves all team members from WhatsBox. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from WhatsBox. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from WhatsBox. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves all webhook subscriptions from WhatsBox. |
| [Upsert Webhook Subscription](actions/upsert-webhook-subscription.md) | POST | Creates or updates a webhook subscription in WhatsBox. |

