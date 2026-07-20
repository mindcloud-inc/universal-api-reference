# <img src="https://images.mindcloud.co/apps/icons/mocean-api_1774969693972.png" alt="Mocean API logo" width="28" height="28"> Mocean API: Universal API

Send SMS and verification codes, run number lookups, place voice calls, and manage WhatsApp templates with Mocean API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moceanAPI/latest
- **Category:** Communication / Team Messaging
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moceanapi.com
- **Vendor API docs:** https://moceanapi.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Hang Up Call](actions/hang-up-call.md) | PUT |  |
| [Voice Call Collect Digits](actions/voice-call-collect-digits.md) | POST |  |
| [Voice Call Play Audio](actions/voice-call-play-audio.md) | POST |  |
| [Voice Call Record Call](actions/voice-call-record-call.md) | POST |  |
| [Voice Call Say Message](actions/voice-call-say-message.md) | POST |  |
| [Voice Call Transfer](actions/voice-call-transfer.md) | POST |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Download WhatsApp Rich Media](actions/download-whatsapp-rich-media.md) | GET |  |
| [Get Message Status](actions/get-message-status.md) | GET |  |
| [Resend Verify Code SMS](actions/resend-verify-code-sms.md) | POST |  |
| [Resend Verify Code SMS With Lookup](actions/resend-verify-code-sms-with-lookup.md) | POST |  |
| [Send Binary SMS](actions/send-binary-sms.md) | POST |  |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST |  |
| [Send Flash SMS](actions/send-flash-sms.md) | POST |  |
| [Send Scheduled SMS](actions/send-scheduled-sms.md) | POST |  |
| [Send SMS](actions/send-sms.md) | POST |  |
| [Send SMS With Delivery Report](actions/send-sms-with-delivery-report.md) | POST |  |
| [Send Unicode SMS](actions/send-unicode-sms.md) | POST |  |
| [Send Verify Code SMS](actions/send-verify-code-sms.md) | POST |  |
| [Send Verify Code SMS With Lookup](actions/send-verify-code-sms-with-lookup.md) | POST |  |
| [Send Verify Code Telegram](actions/send-verify-code-telegram.md) | POST |  |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Request Async Number Lookup](actions/request-async-number-lookup.md) | GET |  |
| [Request Number Lookup](actions/request-number-lookup.md) | GET |  |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Pricing](actions/get-account-pricing.md) | GET |  |
| [Get Number Lookup Pricing](actions/get-number-lookup-pricing.md) | GET |  |
| [Get SMS Pricing](actions/get-sms-pricing.md) | GET |  |
| [Get Verify Pricing](actions/get-verify-pricing.md) | GET |  |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Download Recording](actions/download-recording.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Check Verify Code](actions/check-verify-code.md) | GET |  |
| [Get Balance](actions/get-balance.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create WhatsApp Template](actions/create-whatsapp-template.md) | POST |  |
| [Delete WhatsApp Template](actions/delete-whatsapp-template.md) | DELETE |  |
| [Edit WhatsApp Template](actions/edit-whatsapp-template.md) | PUT |  |
| [Get WhatsApp Template](actions/get-whatsapp-template.md) | GET |  |
| [List WhatsApp Templates](actions/list-whatsapp-templates.md) | GET |  |

