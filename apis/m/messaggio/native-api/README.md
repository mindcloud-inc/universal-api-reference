# Messaggio: Native API Reference

A consolidated summary of Messaggio's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://messaggio.com/api-docs/
- **OpenAPI specification:** https://messaggio.com/messaggio_api_27102025_en.yaml
- **API base URL:** `https://msg.messaggio.com/api/v1`

## Authentication

### Project Login + API Secret

Connect with the Messaggio bulk messaging project login and API secret key.

### Credentials

- **Project Login:** `projectLogin` · required · Messaggio project login copied from the detailed project info.
- **API Secret Key:** `apiKey` · required · Messaggio API secret key generated in the account settings.

Send these headers with each API request:

```http
Messaggio-Login: <projectLogin>
```

[Official authentication documentation](https://messaggio.com/guide/integrations/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Flash Call Code](actions/send-flash-call-code.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send SMS Text](actions/send-sms-text.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Telegram Media + Button](actions/send-telegram-media-button.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Telegram OTP](actions/send-telegram-otp.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Viber Image](actions/send-viber-image.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Viber Text](actions/send-viber-text.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Viber Text + Button](actions/send-viber-text-button.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send Viber Text + Image + Button](actions/send-viber-text-image-button.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send VKontakte Text](actions/send-vkontakte-text.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Audio](actions/send-whatsapp-audio.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Contact](actions/send-whatsapp-contact.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Document](actions/send-whatsapp-document.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Image](actions/send-whatsapp-image.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Location](actions/send-whatsapp-location.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Sticker](actions/send-whatsapp-sticker.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Template](actions/send-whatsapp-template.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Text](actions/send-whatsapp-text.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Send WhatsApp Video](actions/send-whatsapp-video.md) | `POST /send` | [docs](https://messaggio.com/api-docs/) |
| [Validate Credentials](actions/validate-credentials.md) | `GET https://bulk.sms-online.com/` | [docs](https://messaggio.com/messaggio_api_en.pdf) |
