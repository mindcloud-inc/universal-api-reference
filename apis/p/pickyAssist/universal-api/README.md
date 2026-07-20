# <img src="https://images.mindcloud.co/apps/icons/picky-assist_1775575013705.png" alt="Picky Assist logo" width="28" height="28"> Picky Assist: Universal API

Picky Assist helps businesses automate customer communication across modern messaging channels like WhatsApp, Email, Instagram, and Facebook Messenger.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pickyAssist/latest
- **Category:** Marketing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pickyassist.com
- **Vendor API docs:** https://help.pickyassist.com/api-documentation-v2/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET |  |

### Contact Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Contacts](actions/sending-contacts.md) | POST |  |

### Delivery Report

| Action | Method | Description |
| --- | --- | --- |
| [Delivery Report](actions/delivery-report.md) | GET |  |

### Device Status

| Action | Method | Description |
| --- | --- | --- |
| [Fetching Device Status API](actions/fetching-device-status-api.md) | GET |  |

### Document Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Dynamic Document with Dynamic Message](actions/sending-dynamic-document-with-dynamic-message.md) | POST |  |
| [Sending Static Document with Dynamic Message](actions/sending-static-document-with-dynamic-message.md) | POST |  |

### Group Media Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Media Files](actions/sending-media-files.md) | POST |  |

### Group Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Text Message](actions/sending-text-message.md) | POST |  |
| [Sending Text Message with Mention](actions/sending-text-message-with-mention.md) | POST |  |

### Interactive Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Interactive Buttons Image with Call 2 Action URL](actions/sending-interactive-buttons-image-with-call2-action-url.md) | POST |  |
| [Sending Interactive Buttons Text with Quick Replies](actions/sending-interactive-buttons-text-with-quick-replies.md) | POST |  |
| [Sending Interactive Buttons URL & Phone Number](actions/sending-interactive-buttons-url-phone-number.md) | POST |  |

### Location Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Location](actions/sending-location.md) | POST |  |

### Media Message

| Action | Method | Description |
| --- | --- | --- |
| [Sending Dynamic Image with Personalised Text](actions/sending-dynamic-image-with-personalised-text.md) | POST |  |
| [Sending Media Messages - Image Static Caption](actions/sending-media-messages-image-static-caption.md) | POST |  |
| [Sending Media Messages - Image With Dynamic Caption](actions/sending-media-messages-image-with-dynamic-caption.md) | POST |  |
| [Sending Static Image with Dynamic Message](actions/sending-static-image-with-dynamic-message.md) | POST |  |

### Message Batch

| Action | Method | Description |
| --- | --- | --- |
| [Sending Bulk Messages](actions/sending-bulk-messages.md) | POST |  |
| [Sending Dynamic Messages](actions/sending-dynamic-messages.md) | POST |  |

### Template Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status of All Templates](actions/get-status-of-all-templates.md) | GET |  |
| [Template API Status with Template ID](actions/template-api-status-with-template-id.md) | GET |  |

### Two Step Verification

| Action | Method | Description |
| --- | --- | --- |
| [2 Step Verification Disable](actions/step-verification-disable.md) | PUT |  |
| [2 Step Verification Enable](actions/step-verification-enable.md) | PUT |  |

### Whatsapp Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Admin](actions/add-group-admin.md) | PUT |  |
| [Create Group](actions/create-group.md) | POST |  |
| [Fetch Group Details](actions/fetch-group-details.md) | GET |  |
| [Group Delete Actions](actions/group-delete-actions.md) | DELETE |  |
| [Update Group Info](actions/update-group-info.md) | PUT |  |

### Whatsapp Group Invite Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate New Invite Link](actions/generate-new-invite-link.md) | PUT |  |

### Whatsapp Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Remove Group Members / Admin](actions/remove-group-members-admin.md) | DELETE |  |

### Whatsapp Profile

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Profile API](actions/whats-app-profile-api.md) | PUT |  |

### Whatsapp Template

| Action | Method | Description |
| --- | --- | --- |
| [Template API Request - Document](actions/template-api-request-document.md) | POST |  |
| [Template API Request - Image](actions/template-api-request-image.md) | POST |  |
| [Template API Request - Text](actions/template-api-request-text.md) | POST |  |

