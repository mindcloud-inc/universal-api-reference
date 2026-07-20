# Kommunicate: Native API Reference

A consolidated summary of Kommunicate's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.kommunicate.io/
- **API base URL:** `https://services.kommunicate.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.kommunicate.io/docs/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `response`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Conversation Assignee](actions/change-conversation-assignee.md) | `PATCH /rest/ws/group/assignee/change` | [docs](https://docs.kommunicate.io/docs/api-detail#change-conversation-assignee) |
| [Change Conversation Status](actions/change-conversation-status.md) | `PATCH /rest/ws/group/status/change` | [docs](https://docs.kommunicate.io/docs/api-detail#change-conversation-status) |
| [Create Conversation](actions/create-conversation.md) | `POST /rest/ws/group/conversation` | [docs](https://docs.kommunicate.io/docs/api-detail#create-a-conversation) |
| [Create Conversation With Assignee](actions/create-conversation-with-assignee.md) | `POST /rest/ws/group/conversation` | [docs](https://docs.kommunicate.io/docs/api-detail#create-a-conversation) |
| [Get User Detail](actions/get-user-detail.md) | `POST /rest/ws/user/v2/detail` | [docs](https://docs.kommunicate.io/docs/api-detail#get-user-detail) |
| [Send Attachments](actions/send-attachments.md) | `POST /rest/ws/message/send` | [docs](https://docs.kommunicate.io/docs/api-detail#send-attachments) |
| [Send Auto Suggestion Message](actions/send-auto-suggestion-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#autosuggestions-in-your-chat-box) |
| [Send Card Carousel Message](actions/send-card-carousel-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#card-carousel) |
| [Send Custom Input Field Message](actions/send-custom-input-field-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#custom-input-field) |
| [Send Form Template Message](actions/send-form-template-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#form-template) |
| [Send Generic Card Message](actions/send-generic-card-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#generic-card) |
| [Send HTML Content Message](actions/send-html-content-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#html-content) |
| [Send Image Template Message](actions/send-image-template-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#images) |
| [Send Link Button Message](actions/send-link-button-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#link-button) |
| [Send List Template Message](actions/send-list-template-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#list-template) |
| [Send Message](actions/send-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/api-detail#send-message) |
| [Send Mixed Buttons Message](actions/send-mixed-buttons-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#combine-different-type-of-buttons-with-single-message) |
| [Send Submit Button Message](actions/send-submit-button-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#submit-button) |
| [Send Suggested Replies Message](actions/send-suggested-replies-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#suggested-replies) |
| [Send Video Message](actions/send-video-message.md) | `POST /rest/ws/message/v2/send` | [docs](https://docs.kommunicate.io/docs/message-types#videos--youtube) |
| [Update User Details](actions/update-user-details.md) | `POST /rest/ws/user/update` | [docs](https://docs.kommunicate.io/docs/api-detail#update-user-details) |
