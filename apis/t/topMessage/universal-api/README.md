# <img src="https://images.mindcloud.co/apps/icons/logo_1775158757146.png" alt="TopMessage logo" width="28" height="28"> TopMessage: Universal API

Send and retrieve SMS and WhatsApp messages, manage messaging workflows, and track message activity with TopMessage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/topMessage/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://topmessage.com/
- **Vendor API docs:** https://topmessage.com/documentation-api/send-message

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message By ID](actions/get-message-by-id.md) | GET | Retrieves a message by ID from TopMessage. |
| [List Messages](actions/list-messages.md) | GET | Retrieves sent and received messages from TopMessage. |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST | Creates a bulk SMS message in TopMessage. |
| [Send Scheduled SMS](actions/send-scheduled-sms.md) | POST | Creates a scheduled SMS message in TopMessage. |
| [Send Simple SMS](actions/send-simple-sms.md) | POST | Creates a simple SMS message in TopMessage. |
| [Send SMS Template Message](actions/send-sms-template-message.md) | POST | Creates an SMS template message in TopMessage. |
| [Send SMS With Shortened Links](actions/send-sms-with-shortened-links.md) | POST | Creates an SMS message with shortened links in TopMessage. |
| [Send Verification SMS](actions/send-verification-sms.md) | POST | Creates a verification SMS message in TopMessage. |
| [Send WhatsApp Free-form Reply](actions/send-whats-app-free-form-reply.md) | POST | Creates a WhatsApp free-form reply in TopMessage. |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | POST | Creates a WhatsApp template message in TopMessage. |
| [Verify Message Code](actions/verify-message-code.md) | GET | Verifies a message code by recipient number in TopMessage. |

