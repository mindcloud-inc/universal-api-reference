# <img src="https://images.mindcloud.co/apps/icons/d7messaging_1774547699710.png" alt="D7 Messaging logo" width="28" height="28"> D7 Messaging: Universal API

D7 Messaging lets teams send SMS, OTP, WhatsApp, and Viber messages, fetch pricing, and track delivery/status through D7's messaging APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/d7Messaging/latest
- **Category:** Communication / Team Messaging
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://d7networks.com
- **Vendor API docs:** https://d7networks.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get SMS Pricing](actions/get-sms-pricing.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Otp Verification

| Action | Method | Description |
| --- | --- | --- |
| [Get OTP Status](actions/get-otp-status.md) | GET | Retrieves OTP status from D7 Messaging. |
| [Resend OTP](actions/resend-otp.md) | POST | Resends a one-time password through D7 Messaging. |
| [Send OTP](actions/send-otp.md) | POST | Sends a one-time password through D7 Messaging. |
| [Verify OTP](actions/verify-otp.md) | POST | Verifies a one-time password in D7 Messaging. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Status](actions/get-sms-status.md) | GET | Retrieves SMS delivery status from D7 Messaging. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message through D7 Messaging. |

### Sms Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Pricing](actions/get-sms-pricing.md) | GET | Retrieves SMS pricing from D7 Messaging. |

### Viber Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Viber Status](actions/get-viber-status.md) | GET | Retrieves Viber delivery status from D7 Messaging. |
| [Send Viber Message](actions/send-viber-message.md) | POST | Sends a Viber message through D7 Messaging. |

### Whatsapp Media

| Action | Method | Description |
| --- | --- | --- |
| [Download WhatsApp Media](actions/download-whats-app-media.md) | GET | Downloads WhatsApp media from D7 Messaging. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp Status](actions/get-whats-app-status.md) | GET | Retrieves WhatsApp delivery status from D7 Messaging. |
| [Mark WhatsApp Message as Read](actions/mark-whats-app-message-as-read.md) | PUT | Marks a WhatsApp message as read in D7 Messaging. |
| [Send WhatsApp Audio Message](actions/send-whats-app-audio-message.md) | POST | Sends a WhatsApp audio message through D7 Messaging. |
| [Send WhatsApp Authentication Template Message](actions/send-whats-app-authentication-template-message.md) | POST | Sends a WhatsApp authentication template message through D7 Messaging. |
| [Send WhatsApp Carousel Template Message](actions/send-whats-app-carousel-template-message.md) | POST | Sends a WhatsApp carousel template message through D7 Messaging. |
| [Send WhatsApp Contacts Message](actions/send-whats-app-contacts-message.md) | POST | Sends a WhatsApp contacts message through D7 Messaging. |
| [Send WhatsApp Custom Template Message](actions/send-whats-app-custom-template-message.md) | POST | Sends a WhatsApp custom template message through D7 Messaging. |
| [Send WhatsApp Document Message](actions/send-whats-app-document-message.md) | POST | Sends a WhatsApp document message through D7 Messaging. |
| [Send WhatsApp Flows Template Message](actions/send-whats-app-flows-template-message.md) | POST | Sends a WhatsApp flows template message through D7 Messaging. |
| [Send WhatsApp Generic Attachment Message](actions/send-whats-app-generic-attachment-message.md) | POST | Sends a WhatsApp attachment message through D7 Messaging. |
| [Send WhatsApp Image Message](actions/send-whats-app-image-message.md) | POST | Sends a WhatsApp image message through D7 Messaging. |
| [Send WhatsApp Interactive CTA URL Message](actions/send-whats-app-interactive-ctaurl-message.md) | POST | Sends a WhatsApp interactive CTA URL message through D7 Messaging. |
| [Send WhatsApp Limited Time Offer Template Message](actions/send-whats-app-limited-time-offer-template-message.md) | POST | Sends a WhatsApp limited-time offer template message through D7 Messaging. |
| [Send WhatsApp Location Message](actions/send-whats-app-location-message.md) | POST | Sends a WhatsApp location message through D7 Messaging. |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | POST | Sends a WhatsApp text message through D7 Messaging. |
| [Send WhatsApp Video Message](actions/send-whats-app-video-message.md) | POST | Sends a WhatsApp video message through D7 Messaging. |

