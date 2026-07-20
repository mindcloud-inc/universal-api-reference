# <img src="https://images.mindcloud.co/apps/icons/kommunicate_1774383368862.png" alt="Kommunicate logo" width="28" height="28"> Kommunicate: Universal API

Manage support conversations, users, messages, and agent routing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kommunicate/latest
- **Category:** Support / Contact Center
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kommunicate.io
- **Vendor API docs:** https://docs.kommunicate.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Detail](actions/get-user-detail.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userIdList%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Change Conversation Assignee](actions/change-conversation-assignee.md) | PUT | Updates a conversation assignee in Kommunicate. |
| [Change Conversation Status](actions/change-conversation-status.md) | PUT | Updates a conversation status in Kommunicate. |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Kommunicate. |
| [Create Conversation With Assignee](actions/create-conversation-with-assignee.md) | POST | Creates a new conversation with an assignee in Kommunicate. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Attachments](actions/send-attachments.md) | POST | Creates an attachment message in Kommunicate. |
| [Send HTML Content Message](actions/send-html-content-message.md) | POST | Creates an HTML content message in Kommunicate. |
| [Send Image Template Message](actions/send-image-template-message.md) | POST | Creates an image template message in Kommunicate. |
| [Send Link Button Message](actions/send-link-button-message.md) | POST | Creates a link button message in Kommunicate. |
| [Send Message](actions/send-message.md) | POST | Creates a message in Kommunicate. |
| [Send Mixed Buttons Message](actions/send-mixed-buttons-message.md) | POST | Creates a mixed buttons message in Kommunicate. |
| [Send Submit Button Message](actions/send-submit-button-message.md) | POST | Creates a submit button message in Kommunicate. |
| [Send Suggested Replies Message](actions/send-suggested-replies-message.md) | POST | Creates a suggested replies message in Kommunicate. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Auto Suggestion Message](actions/send-auto-suggestion-message.md) | POST | Creates an auto suggestion message in Kommunicate. |
| [Send Card Carousel Message](actions/send-card-carousel-message.md) | POST | Creates a card carousel message in Kommunicate. |
| [Send Custom Input Field Message](actions/send-custom-input-field-message.md) | POST | Creates a custom input field message in Kommunicate. |
| [Send Form Template Message](actions/send-form-template-message.md) | POST | Creates a form template message in Kommunicate. |
| [Send Generic Card Message](actions/send-generic-card-message.md) | POST | Creates a generic card message in Kommunicate. |
| [Send List Template Message](actions/send-list-template-message.md) | POST | Creates a list template message in Kommunicate. |
| [Send Video Message](actions/send-video-message.md) | POST | Creates a video message in Kommunicate. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Detail](actions/get-user-detail.md) | GET | Retrieves user details from Kommunicate. |
| [Update User Details](actions/update-user-details.md) | PUT | Updates an existing user in Kommunicate. |

