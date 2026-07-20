# Picky Assist: Native API Reference

A consolidated summary of Picky Assist's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://help.pickyassist.com/api-documentation-v2/introduction
- **API base URL:** `https://app.pickyassist.com/api/v2`

## Authentication

### API Key

Authenticate Picky Assist requests by sending the API token in the JSON request body as `token`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.pickyassist.com/api-documentation-v2/quick-start-guide)

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Group Admin](actions/add-group-admin.md) | `POST /add-group-admin` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Create Group](actions/create-group.md) | `POST /create-whatsapp-group` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Delivery Report](actions/delivery-report.md) | `POST /delivery-report` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/delivery-reports) |
| [Fetch Group Details](actions/fetch-group-details.md) | `POST /group-details` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Fetching Device Status API](actions/fetching-device-status-api.md) | `POST /device-status` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Generate New Invite Link](actions/generate-new-invite-link.md) | `POST /generate-invite-link` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Get Account Balance](actions/get-account-balance.md) | `POST /check-balance` | [docs](https://help.pickyassist.com/api-documentation-v2/account-api/fetch-balance) |
| [Get Status of All Templates](actions/get-status-of-all-templates.md) | `POST /template-status` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-status-api) |
| [Group Delete Actions](actions/group-delete-actions.md) | `POST /delete-group-action` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Remove Group Members / Admin](actions/remove-group-members-admin.md) | `POST /remove-group-members` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Sending Bulk Messages](actions/sending-bulk-messages.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-bulk-messages-push) |
| [Sending Contacts](actions/sending-contacts.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-contacts) |
| [Sending Dynamic Document with Dynamic Message](actions/sending-dynamic-document-with-dynamic-message.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Dynamic Image with Personalised Text](actions/sending-dynamic-image-with-personalised-text.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Dynamic Messages](actions/sending-dynamic-messages.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-dynamic-messages-push) |
| [Sending Interactive Buttons Image with Call 2 Action URL](actions/sending-interactive-buttons-image-with-call2-action-url.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-interactive-list-and-buttons) |
| [Sending Interactive Buttons Text with Quick Replies](actions/sending-interactive-buttons-text-with-quick-replies.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-interactive-list-and-buttons) |
| [Sending Interactive Buttons URL & Phone Number](actions/sending-interactive-buttons-url-phone-number.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-interactive-list-and-buttons) |
| [Sending Location](actions/sending-location.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-location) |
| [Sending Media Files](actions/sending-media-files.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Sending Media Messages - Image Static Caption](actions/sending-media-messages-image-static-caption.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Media Messages - Image With Dynamic Caption](actions/sending-media-messages-image-with-dynamic-caption.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Static Document with Dynamic Message](actions/sending-static-document-with-dynamic-message.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Static Image with Dynamic Message](actions/sending-static-image-with-dynamic-message.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push) |
| [Sending Text Message](actions/sending-text-message.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [Sending Text Message with Mention](actions/sending-text-message-with-mention.md) | `POST /push` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [2 Step Verification Disable](actions/step-verification-disable.md) | `POST /two-step-verification` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-settings-apis/2-step-verification) |
| [2 Step Verification Enable](actions/step-verification-enable.md) | `POST /two-step-verification` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-settings-apis/2-step-verification) |
| [Template API Request - Document](actions/template-api-request-document.md) | `POST /template-request` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-request-api) |
| [Template API Request - Image](actions/template-api-request-image.md) | `POST /template-request` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-request-api) |
| [Template API Request - Text](actions/template-api-request-text.md) | `POST /template-request` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-request-api) |
| [Template API Status with Template ID](actions/template-api-status-with-template-id.md) | `POST /template-status` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-status-api) |
| [Update Group Info](actions/update-group-info.md) | `POST /update-group-info` | [docs](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis) |
| [WhatsApp Profile API](actions/whats-app-profile-api.md) | `POST /update-profile` | [docs](https://help.pickyassist.com/api-documentation-v2/whatsapp-settings-apis/whatsapp-profile-api) |
