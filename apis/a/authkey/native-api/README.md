# Authkey: Native API Reference

A consolidated summary of Authkey's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://authkey.io/api-docs
- **API base URL:** `https://console.authkey.io/restapi`

## Authentication

### API Key

Connect using the Authkey dashboard authkey.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://authkey.io/whatsapp-api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | `GET /getbalance.php` | [docs](https://authkey.io/whatsapp-api-docs) |
| [Send Email From Template](actions/send-email-from-template.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/email-api-docs) |
| [Send International SMS](actions/send-international-sms.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS](actions/send-sms.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS And Voice In Parallel](actions/send-sms-and-voice-in-parallel.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS From Template](actions/send-sms-from-template.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS From Template (POST)](actions/send-sms-from-template-post.md) | `POST https://console.authkey.io/restapi/requestjson.php` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS (POST)](actions/send-sms-post.md) | `POST https://console.authkey.io/restapi/requestjson.php` | [docs](https://authkey.io/sms-api-docs/) |
| [Send SMS With Voice Fallback](actions/send-sms-with-voice-fallback.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send Unicode SMS](actions/send-unicode-sms.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Send Voice Call](actions/send-voice-call.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/voice-api-docs) |
| [Send Voice Call From Template](actions/send-voice-call-from-template.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/voice-api-docs) |
| [Send Voice With SMS Fallback](actions/send-voice-with-sms-fallback.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/voice-api-docs) |
| [Send WhatsApp Media Template](actions/send-whats-app-media-template.md) | `GET https://console.authkey.io/restapi/request.php` | [docs](https://authkey.io/whatsapp-api-docs) |
| [Send WhatsApp Media Template (POST)](actions/send-whats-app-media-template-post.md) | `POST https://console.authkey.io/restapi/requestjson.php` | [docs](https://authkey.io/whatsapp-api-docs) |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | `GET https://console.authkey.io/restapi/request.php` | [docs](https://authkey.io/whatsapp-api-docs) |
| [Send WhatsApp Template Message (POST)](actions/send-whats-app-template-message-post.md) | `POST https://console.authkey.io/restapi/requestjson.php` | [docs](https://authkey.io/whatsapp-api-docs) |
| [Start 2FA Session](actions/start2fa-session.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/2fa-api-docs) |
| [Trigger Email Event](actions/trigger-email-event.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/email-api-docs) |
| [Trigger Messaging Event By Mobile](actions/trigger-messaging-event-by-mobile.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/sms-api-docs/) |
| [Trigger Messaging Event By Mobile And Email](actions/trigger-messaging-event-by-mobile-and-email.md) | `GET https://api.authkey.io/request` | [docs](https://authkey.io/voice-api-docs) |
| [Verify 2FA OTP](actions/verify2fa-otp.md) | `GET https://console.authkey.io/api/2fa_verify.php` | [docs](https://authkey.io/2fa-api-docs) |
