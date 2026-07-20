# <img src="https://images.mindcloud.co/apps/icons/favicon-7_1775072706393.png" alt="Messaggio logo" width="28" height="28"> Messaggio: Universal API

Messaggio is a multichannel messaging platform for SMS and Viber delivery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/messaggio/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://messaggio.com/
- **Vendor API docs:** https://messaggio.com/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Credentials](actions/validate-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Flash Call Code](actions/send-flash-call-code.md) | POST | Creates a flash call code in Messaggio. |
| [Send SMS Text](actions/send-sms-text.md) | POST | Creates an SMS text message in Messaggio. |
| [Send Telegram Media + Button](actions/send-telegram-media-button.md) | POST | Creates a Telegram media message with a button in Messaggio. |
| [Send Telegram OTP](actions/send-telegram-otp.md) | POST | Creates a Telegram OTP message in Messaggio. |
| [Send Viber Image](actions/send-viber-image.md) | POST | Creates a Viber image message in Messaggio. |
| [Send Viber Text](actions/send-viber-text.md) | POST | Creates a Viber text message in Messaggio. |
| [Send Viber Text + Button](actions/send-viber-text-button.md) | POST | Creates a Viber text message with a button in Messaggio. |
| [Send Viber Text + Image + Button](actions/send-viber-text-image-button.md) | POST | Creates a Viber image message with a button in Messaggio. |
| [Send VKontakte Text](actions/send-vkontakte-text.md) | POST | Creates a VKontakte text message in Messaggio. |
| [Send WhatsApp Audio](actions/send-whatsapp-audio.md) | POST | Creates a WhatsApp audio message in Messaggio. |
| [Send WhatsApp Contact](actions/send-whatsapp-contact.md) | POST | Creates a WhatsApp contact message in Messaggio. |
| [Send WhatsApp Document](actions/send-whatsapp-document.md) | POST | Creates a WhatsApp document message in Messaggio. |
| [Send WhatsApp Image](actions/send-whatsapp-image.md) | POST | Creates a WhatsApp image message in Messaggio. |
| [Send WhatsApp Location](actions/send-whatsapp-location.md) | POST | Creates a WhatsApp location message in Messaggio. |
| [Send WhatsApp Sticker](actions/send-whatsapp-sticker.md) | POST | Creates a WhatsApp sticker message in Messaggio. |
| [Send WhatsApp Template](actions/send-whatsapp-template.md) | POST | Creates a WhatsApp template message in Messaggio. |
| [Send WhatsApp Text](actions/send-whatsapp-text.md) | POST | Creates a WhatsApp text message in Messaggio. |
| [Send WhatsApp Video](actions/send-whatsapp-video.md) | POST | Creates a WhatsApp video message in Messaggio. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Validate Credentials](actions/validate-credentials.md) | GET | Validates stored Messaggio credentials against the bulk API. |

