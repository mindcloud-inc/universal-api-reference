# <img src="https://images.mindcloud.co/apps/icons/id3vao9p9s-logos_1775069336784.png" alt="Authkey logo" width="28" height="28"> Authkey: Universal API

Send and verify messages across SMS, voice, email, and WhatsApp

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/authkey/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://authkey.io
- **Vendor API docs:** https://authkey.io/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves the current account balance from Authkey. |

### Email Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Email From Template](actions/send-email-from-template.md) | POST | Sends a templated email through Authkey. |

### Messaging Event

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Email Event](actions/trigger-email-event.md) | POST | Triggers an email event in Authkey. |
| [Trigger Messaging Event By Mobile](actions/trigger-messaging-event-by-mobile.md) | POST | Triggers a messaging event for a mobile number in Authkey. |
| [Trigger Messaging Event By Mobile And Email](actions/trigger-messaging-event-by-mobile-and-email.md) | POST | Triggers a messaging event by mobile and email in Authkey. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send International SMS](actions/send-international-sms.md) | POST | Sends an international SMS through Authkey. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message through Authkey. |
| [Send SMS And Voice In Parallel](actions/send-sms-and-voice-in-parallel.md) | POST | Sends SMS and voice messages in parallel through Authkey. |
| [Send SMS From Template](actions/send-sms-from-template.md) | POST | Sends an SMS from a template in Authkey. |
| [Send SMS From Template (POST)](actions/send-sms-from-template-post.md) | POST | Sends an SMS from a template in Authkey. |
| [Send SMS (POST)](actions/send-sms-post.md) | POST | Sends an SMS message through Authkey. |
| [Send SMS With Voice Fallback](actions/send-sms-with-voice-fallback.md) | POST | Sends an SMS with voice fallback through Authkey. |
| [Send Unicode SMS](actions/send-unicode-sms.md) | POST | Sends a Unicode SMS message through Authkey. |

### Two-factor Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Start 2FA Session](actions/start2fa-session.md) | POST | Starts a 2FA session in Authkey. |
| [Verify 2FA OTP](actions/verify2fa-otp.md) | POST | Verifies a 2FA OTP in Authkey. |

### Voice Call

| Action | Method | Description |
| --- | --- | --- |
| [Send Voice Call](actions/send-voice-call.md) | POST | Sends a voice call through Authkey. |
| [Send Voice Call From Template](actions/send-voice-call-from-template.md) | POST | Sends a templated voice call through Authkey. |
| [Send Voice With SMS Fallback](actions/send-voice-with-sms-fallback.md) | POST | Sends a voice call with SMS fallback through Authkey. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Media Template](actions/send-whats-app-media-template.md) | POST | Sends a WhatsApp media template through Authkey. |
| [Send WhatsApp Media Template (POST)](actions/send-whats-app-media-template-post.md) | POST | Sends a WhatsApp media template through Authkey. |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | POST | Sends a WhatsApp template message through Authkey. |
| [Send WhatsApp Template Message (POST)](actions/send-whats-app-template-message-post.md) | POST | Sends a WhatsApp template message through Authkey. |

