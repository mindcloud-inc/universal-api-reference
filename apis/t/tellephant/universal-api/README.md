# <img src="https://images.mindcloud.co/apps/icons/favicon-app-tellephant-com-48x48_1777046544286.png" alt="Tellephant logo" width="28" height="28"> Tellephant: Universal API

Tellephant provides WhatsApp messaging, OTP, contact tagging, unsubscribe, log, and webhook management APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tellephant/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tellephant.com
- **Vendor API docs:** https://app.tellephant.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List incoming logs](actions/list-incoming-logs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs?connectionId=$CONNECTION_ID&startDate=24-04-2026&endDate=24-04-2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Contact Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get contact tags](actions/get-contact-tags.md) | GET | Retrieves tags for a Tellephant contact. |
| [Update contact tags](actions/update-contact-tags.md) | PUT | Updates tags for WhatsApp contacts in Tellephant. |

### Incoming Log

| Action | Method | Description |
| --- | --- | --- |
| [List incoming logs](actions/list-incoming-logs.md) | GET | Retrieves incoming message logs from Tellephant. |

### Message History

| Action | Method | Description |
| --- | --- | --- |
| [Get message history](actions/get-message-history.md) | GET | Retrieves delivery history for a message in Tellephant. |

### Otp

| Action | Method | Description |
| --- | --- | --- |
| [Send OTP](actions/send-otp.md) | POST | Sends an OTP message through Tellephant. |

### Otp Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate OTP](actions/validate-otp.md) | GET | Validates an OTP code in Tellephant. |

### Outgoing Log

| Action | Method | Description |
| --- | --- | --- |
| [List outgoing logs](actions/list-outgoing-logs.md) | GET | Retrieves outgoing message logs from Tellephant. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create tags](actions/create-tags.md) | POST | Creates tags for contacts in Tellephant. |

### Template Log

| Action | Method | Description |
| --- | --- | --- |
| [List template logs](actions/list-template-logs.md) | GET | Retrieves template message logs from Tellephant. |

### Unsubscribe Status

| Action | Method | Description |
| --- | --- | --- |
| [Update unsubscribe status](actions/update-unsubscribe-status.md) | PUT | Updates contact subscription status in Tellephant. |

### Unsubscribed Contact

| Action | Method | Description |
| --- | --- | --- |
| [List unsubscribed contacts](actions/list-unsubscribed-contacts.md) | GET | Retrieves contacts by subscription status from Tellephant. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get webhooks](actions/get-webhooks.md) | GET | Retrieves current webhook settings from Tellephant. |
| [Update webhook](actions/update-webhook.md) | PUT | Updates a webhook configuration in Tellephant. |

### Whatsapp Session Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp session message](actions/send-whats-app-session-message.md) | POST | Sends a WhatsApp session message through Tellephant. |

### Whatsapp Template Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp template message](actions/send-whats-app-template-message.md) | POST | Sends a WhatsApp template message through Tellephant. |

