# <img src="https://images.mindcloud.co/apps/icons/boomerang-messaging-icon-filled-256_1777496140937.png" alt="boomApp Connect logo" width="28" height="28"> boomApp Connect: Universal API

Boost customer engagement with Boomerang SMS, voice, and email messaging workflows through the boomApp Connect API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boomAppConnect/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://boomerangmessaging.com/products/boomapp-connect/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/boomappconnect/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Message Responses](actions/retrieve-message-responses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Delivery Status

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Delivery Status Updates](actions/retrieve-delivery-status-updates.md) | GET | Retrieves outbound delivery status updates from boomApp Connect. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Creates an email message in boomApp Connect. |

### Inbound Message

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Inbound Campaign Messages](actions/retrieve-inbound-campaign-messages.md) | GET | Retrieves inbound campaign messages from boomApp Connect. |

### Masked Two-way Sms Thread

| Action | Method | Description |
| --- | --- | --- |
| [Create Masked Two-Way SMS Thread](actions/create-masked-two-way-sms-thread.md) | POST | Creates a masked two-way SMS thread in boomApp Connect. |

### Message Response

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Message Responses](actions/retrieve-message-responses.md) | GET | Retrieves responses to outbound messages from boomApp Connect. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS From Custom Number](actions/send-sms-from-custom-number.md) | POST | Creates an SMS message from a custom number in boomApp Connect. |
| [Send SMS One-Way](actions/send-sms-one-way.md) | POST | Creates a one-way SMS message in boomApp Connect. |
| [Send SMS Two-Way](actions/send-sms-two-way.md) | POST | Creates a two-way SMS message in boomApp Connect. |

### Voice Call

| Action | Method | Description |
| --- | --- | --- |
| [Make Voice Call](actions/make-voice-call.md) | POST | Creates a text-to-speech voice call in boomApp Connect. |

