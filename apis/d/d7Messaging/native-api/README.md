# D7 Messaging: Native API Reference

A consolidated summary of D7 Messaging's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://d7networks.com/docs/
- **API base URL:** `https://api.d7networks.com`

## Authentication

### Bearer Token

Use a D7 bearer token in the Authorization header. D7 issues the token from the application login endpoint using a client_id and client_secret.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://d7networks.com/docs/authentication/generate-token/)

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download WhatsApp Media](actions/download-whats-app-media.md) | `GET /whatsapp/v2/download/:media_id` | [docs](https://d7networks.com/docs/whatsapp/download-media/) |
| [Get OTP Status](actions/get-otp-status.md) | `GET /verify/v1/report/:otp_id` | [docs](https://d7networks.com/docs/verify/get-status/) |
| [Get SMS Pricing](actions/get-sms-pricing.md) | `GET /messages/v1/sms/pricing` | [docs](https://d7networks.com/docs/sms/pricing/) |
| [Get SMS Status](actions/get-sms-status.md) | `GET /report/v1/message-log/:request_id` | [docs](https://d7networks.com/docs/sms/get-status/) |
| [Get Viber Status](actions/get-viber-status.md) | `GET /report/v1/viber-log/:request_id` | [docs](https://d7networks.com/docs/viber/get-status/) |
| [Get WhatsApp Status](actions/get-whats-app-status.md) | `GET /whatsapp/v2/report/:request_id` | [docs](https://d7networks.com/docs/whatsapp/get-status/) |
| [Mark WhatsApp Message as Read](actions/mark-whats-app-message-as-read.md) | `POST /whatsapp/v2/read-receipt/:message_id` | [docs](https://d7networks.com/docs/whatsapp/read-receipt/) |
| [Resend OTP](actions/resend-otp.md) | `POST /verify/v1/otp/resend-otp` | [docs](https://d7networks.com/docs/verify/resend-otp/) |
| [Send OTP](actions/send-otp.md) | `POST /verify/v1/otp/send-otp` | [docs](https://d7networks.com/docs/verify/send-otp/) |
| [Send SMS](actions/send-sms.md) | `POST /messages/v1/send` | [docs](https://d7networks.com/docs/sms/send-sms/) |
| [Send Viber Message](actions/send-viber-message.md) | `POST /viber/v1/send` | [docs](https://d7networks.com/docs/viber/send-viber-message/) |
| [Send WhatsApp Audio Message](actions/send-whats-app-audio-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/media-message/) |
| [Send WhatsApp Authentication Template Message](actions/send-whats-app-authentication-template-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-templated-message/authentication-template-message/) |
| [Send WhatsApp Carousel Template Message](actions/send-whats-app-carousel-template-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-templated-message/carousel-template-message/) |
| [Send WhatsApp Contacts Message](actions/send-whats-app-contacts-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/contacts-message/) |
| [Send WhatsApp Custom Template Message](actions/send-whats-app-custom-template-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-templated-message/custom-template-messages/) |
| [Send WhatsApp Document Message](actions/send-whats-app-document-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/media-message/) |
| [Send WhatsApp Flows Template Message](actions/send-whats-app-flows-template-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-templated-message/flows-template-message/) |
| [Send WhatsApp Generic Attachment Message](actions/send-whats-app-generic-attachment-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/media-message/) |
| [Send WhatsApp Image Message](actions/send-whats-app-image-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/media-message/) |
| [Send WhatsApp Interactive CTA URL Message](actions/send-whats-app-interactive-ctaurl-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/interactive-message/) |
| [Send WhatsApp Limited Time Offer Template Message](actions/send-whats-app-limited-time-offer-template-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-templated-message/lto-template-messages/) |
| [Send WhatsApp Location Message](actions/send-whats-app-location-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/location-message/) |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/text-message/) |
| [Send WhatsApp Video Message](actions/send-whats-app-video-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/media-message/) |
| [Verify OTP](actions/verify-otp.md) | `POST /verify/v1/otp/verify-otp` | [docs](https://d7networks.com/docs/verify/verify-otp/) |
