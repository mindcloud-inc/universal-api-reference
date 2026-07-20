# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-22-as-13_1776875492762.png" alt="Gupshup logo" width="28" height="28"> Gupshup: Universal API

Gupshup WhatsApp messaging, template, business profile, subscription, and user-management APIs for building and operating WhatsApp Business conversations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gupshup/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gupshup.io
- **Vendor API docs:** https://docs.gupshup.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Templates For App](actions/get-all-templates-for-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Mark Message As Read](actions/mark-message-as-read.md) | PUT | Marks a message as read in Gupshup. |
| [Send Authentication Template Message](actions/send-authentication-template-message.md) | POST | Sends an authentication template WhatsApp message through Gupshup. |
| [Send Carousel Template Message](actions/send-carousel-template-message.md) | POST | Sends a carousel template WhatsApp message through Gupshup. |
| [Send Catalog Message](actions/send-catalog-message.md) | POST | Sends a catalog WhatsApp message through Gupshup. |
| [Send Catalog Template Message](actions/send-catalog-template-message.md) | POST | Sends a catalog template WhatsApp message through Gupshup. |
| [Send Contact Message](actions/send-contact-message.md) | POST | Sends a contact WhatsApp message through Gupshup. |
| [Send Copy Coupon Code Template Message](actions/send-copy-coupon-code-template-message.md) | POST | Sends a copy coupon code template through Gupshup. |
| [Send CTA Template Message](actions/send-cta-template-message.md) | POST | Sends a CTA template WhatsApp message through Gupshup. |
| [Send CTA URL Message](actions/send-cta-url-message.md) | POST | Sends a CTA URL WhatsApp message through Gupshup. |
| [Send Document Template Message](actions/send-document-template-message.md) | POST | Sends a document template WhatsApp message through Gupshup. |
| [Send File Message](actions/send-file-message.md) | POST | Sends a file WhatsApp message through Gupshup. |
| [Send Image Message](actions/send-image-message.md) | POST | Sends an image WhatsApp message through Gupshup. |
| [Send Image Template Message](actions/send-image-template-message.md) | POST | Sends an image template WhatsApp message through Gupshup. |
| [Send List Message](actions/send-list-message.md) | POST | Sends a list WhatsApp message through Gupshup. |
| [Send Location Message](actions/send-location-message.md) | POST | Sends a location WhatsApp message through Gupshup. |
| [Send Location Template Message](actions/send-location-template-message.md) | POST | Sends a location template WhatsApp message through Gupshup. |
| [Send Message](actions/send-message.md) | POST | Sends a WhatsApp message through Gupshup. |
| [Send Multi Product Message](actions/send-multi-product-message.md) | POST | Sends a multi-product WhatsApp message through Gupshup. |
| [Send Quick Reply File Message](actions/send-quick-reply-file-message.md) | POST | Sends a quick reply file message through Gupshup. |
| [Send Quick Reply Media Message](actions/send-quick-reply-media-message.md) | POST | Sends a quick reply media message through Gupshup. |
| [Send Quick Reply Message](actions/send-quick-reply-message.md) | POST | Sends a quick reply WhatsApp message through Gupshup. |
| [Send Quick Reply Template Message](actions/send-quick-reply-template-message.md) | POST | Sends a quick reply template message through Gupshup. |
| [Send Single Product Message](actions/send-single-product-message.md) | POST | Sends a single product WhatsApp message through Gupshup. |
| [Send Sticker Message](actions/send-sticker-message.md) | POST | Sends a sticker WhatsApp message through Gupshup. |
| [Send Template Message](actions/send-template-message.md) | POST | Sends a template WhatsApp message through Gupshup. |
| [Send Text Message](actions/send-text-message.md) | POST | Sends a text WhatsApp message through Gupshup. |
| [Send Text Template Message](actions/send-text-template-message.md) | POST | Sends a text template WhatsApp message through Gupshup. |
| [Send Video Message](actions/send-video-message.md) | POST | Sends a video WhatsApp message through Gupshup. |
| [Send Video Template Message](actions/send-video-template-message.md) | POST | Sends a video template WhatsApp message through Gupshup. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Gupshup. |
| [Create Template With Buttons](actions/create-template-with-buttons.md) | POST | Creates a template with buttons in Gupshup. |
| [Get All Templates For App](actions/get-all-templates-for-app.md) | GET | Retrieves all templates for a Gupshup app. |
| [Get Template By Template ID](actions/get-template-by-template-id.md) | GET | Retrieves a template by template ID from Gupshup. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Delete Business Profile Photo](actions/delete-business-profile-photo.md) | DELETE | Deletes the business profile photo from Gupshup. |
| [Get Business Profile About](actions/get-business-profile-about.md) | GET | Retrieves the business profile about text from Gupshup. |
| [Get Business Profile Details](actions/get-business-profile-details.md) | GET | Retrieves business profile details from Gupshup. |
| [Get Business Profile Photo](actions/get-business-profile-photo.md) | GET | Retrieves the business profile photo from Gupshup. |
| [Update Business Profile About](actions/update-business-profile-about.md) | PUT | Updates the business profile about text in Gupshup. |
| [Update Business Profile Details](actions/update-business-profile-details.md) | PUT | Updates business profile details in Gupshup. |
| [Update Business Profile Photo](actions/update-business-profile-photo.md) | PUT | Updates the business profile photo in Gupshup. |

