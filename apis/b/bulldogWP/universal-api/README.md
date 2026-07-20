# <img src="https://images.mindcloud.co/apps/icons/bulldog-wp_1776794755404.png" alt="Bulldog-WP logo" width="28" height="28"> Bulldog-WP: Universal API

Bulldog-WP is a WhatsApp inbox and automation platform API for managing messages, devices, contacts, campaigns, files, templates, and chat operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bulldogWP/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bulldog-wp.co.il/
- **Vendor API docs:** https://console.bulldog-wp.co.il/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get session health](actions/device-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get analytics](actions/get-analytics.md) | GET | Retrieves analytics from Bulldog-WP. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Bulldog-WP. |
| [Get campaigns](actions/get-campaigns.md) | GET | Retrieves campaigns from Bulldog-WP. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get chat by WID](actions/get-device-chat-details.md) | GET | Retrieves a chat from Bulldog-WP. |
| [Search chats](actions/get-device-chats.md) | GET | Finds chats in Bulldog-WP. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List campaign contacts](actions/get-campaign-contacts.md) | GET | Retrieves campaign contacts from Bulldog-WP. |
| [Get contact](actions/get-device-contact-details.md) | GET | Retrieves a contact from Bulldog-WP. |
| [List contacts](actions/get-device-contacts.md) | GET | Retrieves contacts from Bulldog-WP. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get number by ID](actions/get-device-by-id.md) | GET | Retrieves a phone number from Bulldog-WP. |
| [Get numbers](actions/get-devices.md) | GET | Retrieves phone numbers from Bulldog-WP. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download file content](actions/download-file.md) | GET | Downloads file content from Bulldog-WP. |
| [Get inbound file details](actions/get-device-file-details.md) | GET | Retrieves inbound file details from Bulldog-WP. |
| [Search inbound files](actions/get-device-files.md) | GET | Finds inbound files in Bulldog-WP. |
| [Get file information](actions/get-file.md) | GET | Retrieves file details from Bulldog-WP. |
| [Preview image](actions/preview-file.md) | GET | Retrieves an image preview from Bulldog-WP. |
| [Search files](actions/search-files.md) | GET | Finds files in Bulldog-WP. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List labels](actions/get-labels.md) | GET | Retrieves labels from Bulldog-WP. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Search chat messages](actions/get-chat-messages.md) | GET | Finds chat messages in Bulldog-WP. |
| [Get message details](actions/get-device-message-details.md) | GET | Retrieves message details from Bulldog-WP. |
| [Get message by ID](actions/get-message.md) | GET | Retrieves a message from Bulldog-WP. |
| [Search messages](actions/search-messages.md) | GET | Finds messages in Bulldog-WP. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Check number exists](actions/number-exists.md) | GET | Checks whether phone numbers exist in Bulldog-WP. |
| [Validate numbers](actions/validate-numbers.md) | GET | Validates phone numbers in Bulldog-WP. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Get messaging prices](actions/get-waba-prices.md) | GET | Retrieves messaging prices from Bulldog-WP. |

### Session Health

| Action | Method | Description |
| --- | --- | --- |
| [Get session health](actions/device-health.md) | GET | Retrieves session health from Bulldog-WP. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List templates](actions/get-templates.md) | GET | Retrieves templates from Bulldog-WP. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get users](actions/get-team-users.md) | GET | Retrieves users from Bulldog-WP. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get webhook details](actions/get-webhook.md) | GET | Retrieves a webhook from Bulldog-WP. |
| [Get webhooks](actions/get-webhooks.md) | GET | Retrieves webhooks from Bulldog-WP. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [Get webhook logs](actions/get-webhook-logs.md) | GET | Retrieves webhook logs from Bulldog-WP. |

