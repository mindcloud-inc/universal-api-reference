# Gupshup: Native API Reference

A consolidated summary of Gupshup's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.gupshup.io/reference
- **API base URL:** `https://api.gupshup.io`

## Authentication

### API Key

Authenticate Gupshup API requests with the account API key in the documented `apikey` request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gupshup.io/reference/msg)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | `POST /wa/app/{app_id}/template` | [docs](https://docs.gupshup.io/docs/create-template) |
| [Create Template With Buttons](actions/create-template-with-buttons.md) | `POST /wa/app/{app_id}/template` | [docs](https://docs.gupshup.io/docs/template-button-list) |
| [Delete Business Profile Photo](actions/delete-business-profile-photo.md) | `DELETE /wa/app/{appId}/business/profile/photo` | [docs](https://docs.gupshup.io/reference/delete-profile-photo) |
| [Get All Templates For App](actions/get-all-templates-for-app.md) | `GET /wa/app/{app_id}/template` | [docs](https://docs.gupshup.io/reference/get-all-templates-for-an-app) |
| [Get Business Profile About](actions/get-business-profile-about.md) | `GET /wa/app/{appId}/business/profile/about` | [docs](https://docs.gupshup.io/reference/get-profile-about) |
| [Get Business Profile Details](actions/get-business-profile-details.md) | `GET /wa/app/{appId}/business/profile` | [docs](https://docs.gupshup.io/reference/get-profile-details) |
| [Get Business Profile Photo](actions/get-business-profile-photo.md) | `GET /wa/app/{appId}/business/profile/photo` | [docs](https://docs.gupshup.io/reference/get-profile-photo) |
| [Get Template By Template ID](actions/get-template-by-template-id.md) | `GET /wa/app/{app_id}/template/{template_id}` | [docs](https://docs.gupshup.io/reference/get-template-by-template-id) |
| [Mark Message As Read](actions/mark-message-as-read.md) | `PUT /wa/app/{appId}/msg/{msgId}/read` | [docs](https://docs.gupshup.io/reference/mark-message-as-read) |
| [Send Authentication Template Message](actions/send-authentication-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/authentication-template) |
| [Send Carousel Template Message](actions/send-carousel-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/reference/sending-carousel-template-1) |
| [Send Catalog Message](actions/send-catalog-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/docs/send-catalog-message) |
| [Send Catalog Template Message](actions/send-catalog-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/catalog-template) |
| [Send Contact Message](actions/send-contact-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Copy Coupon Code Template Message](actions/send-copy-coupon-code-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/copy-code) |
| [Send CTA Template Message](actions/send-cta-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send CTA URL Message](actions/send-cta-url-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/cta-url) |
| [Send Document Template Message](actions/send-document-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send File Message](actions/send-file-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Image Message](actions/send-image-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Image Template Message](actions/send-image-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send List Message](actions/send-list-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Location Message](actions/send-location-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Location Template Message](actions/send-location-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send Message](actions/send-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Multi Product Message](actions/send-multi-product-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/docs/send-multi-product-message) |
| [Send Quick Reply File Message](actions/send-quick-reply-file-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Quick Reply Media Message](actions/send-quick-reply-media-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Quick Reply Message](actions/send-quick-reply-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Quick Reply Template Message](actions/send-quick-reply-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send Single Product Message](actions/send-single-product-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/docs/send-single-product-message) |
| [Send Sticker Message](actions/send-sticker-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Template Message](actions/send-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send Text Message](actions/send-text-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Text Template Message](actions/send-text-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Send Video Message](actions/send-video-message.md) | `POST /wa/api/v1/msg` | [docs](https://docs.gupshup.io/reference/msg) |
| [Send Video Template Message](actions/send-video-template-message.md) | `POST /wa/api/v1/template/msg` | [docs](https://docs.gupshup.io/docs/template-messages) |
| [Update Business Profile About](actions/update-business-profile-about.md) | `PUT /wa/app/{appId}/business/profile/about` | [docs](https://docs.gupshup.io/reference/set-profile-about) |
| [Update Business Profile Details](actions/update-business-profile-details.md) | `PUT /wa/app/{appId}/business/profile` | [docs](https://docs.gupshup.io/reference/set-profile-details) |
| [Update Business Profile Photo](actions/update-business-profile-photo.md) | `PUT /wa/app/{appId}/business/profile/photo` | [docs](https://docs.gupshup.io/reference/set-profile-photo) |
