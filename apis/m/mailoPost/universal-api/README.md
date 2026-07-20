# <img src="https://images.mindcloud.co/apps/icons/mailo-post_1776786931924.png" alt="MailoPost logo" width="28" height="28"> MailoPost: Universal API

MailoPost is an email marketing and transactional email service for managing recipient lists, templates, campaigns, organizations, message webhooks, and account balance through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailoPost/latest
- **Category:** Communication / Email Communications
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailopost.ru
- **Vendor API docs:** https://mailopost.ru/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves account balance details from MailoPost. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in MailoPost. |
| [Deliver Campaign](actions/deliver-campaign.md) | PUT | Delivers a MailoPost campaign immediately. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from MailoPost. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from MailoPost. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a MailoPost campaign for delivery. |

### Email Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Message](actions/get-email-message.md) | GET | Retrieves an email message from MailoPost. |
| [Send Email Message](actions/send-email-message.md) | POST | Sends an email message in MailoPost. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST | Creates a new email template in MailoPost. |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template from MailoPost. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from MailoPost. |
| [Submit Email Template For Moderation](actions/submit-email-template-for-moderation.md) | PUT | Submits an email template for moderation in MailoPost. |

### Message Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Message Webhook](actions/create-message-webhook.md) | POST | Creates a new message webhook in MailoPost. |
| [Delete Message Webhook](actions/delete-message-webhook.md) | DELETE | Deletes an existing message webhook from MailoPost. |
| [Get Message Webhook](actions/get-message-webhook.md) | GET | Retrieves a message webhook from MailoPost. |
| [List Message Webhooks](actions/list-message-webhooks.md) | GET | Retrieves message webhooks from MailoPost. |
| [Update Message Webhook](actions/update-message-webhook.md) | PUT | Updates an existing message webhook in MailoPost. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in MailoPost. |
| [Get Current Organization](actions/get-current-organization.md) | GET | Retrieves the current organization from MailoPost. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from MailoPost. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from MailoPost. |
| [Set Current Organization](actions/set-current-organization.md) | PUT | Sets the current organization in MailoPost. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in MailoPost. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in a MailoPost list. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves a recipient from a MailoPost list. |
| [List Recipients](actions/list-recipients.md) | GET | Retrieves recipients from a MailoPost list. |
| [Search Recipients](actions/search-recipients.md) | GET | Finds recipients in MailoPost by email address. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in a MailoPost list. |

### Recipient Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Recipients](actions/import-recipients.md) | POST | Imports recipients into a MailoPost list. |

### Recipient List

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient List](actions/create-recipient-list.md) | POST | Creates a new recipient list in MailoPost. |
| [Get Recipient List](actions/get-recipient-list.md) | GET | Retrieves a recipient list from MailoPost. |
| [List Recipient Lists](actions/list-recipient-lists.md) | GET | Retrieves recipient lists from MailoPost. |
| [Update Recipient List](actions/update-recipient-list.md) | PUT | Updates an existing recipient list in MailoPost. |

### Recipient List Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient List Parameter](actions/create-recipient-list-parameter.md) | POST | Creates a new recipient list parameter in MailoPost. |
| [List Recipient List Parameters](actions/list-recipient-list-parameters.md) | GET | Retrieves recipient list parameters from MailoPost. |
| [Update Recipient List Parameter](actions/update-recipient-list-parameter.md) | PUT | Updates an existing recipient list parameter in MailoPost. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from MailoPost. |

### Template Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Email Template Message](actions/send-email-template-message.md) | POST | Sends an email from a MailoPost template. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves message webhook events from MailoPost. |

### Webhook Message Kind

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Message Kinds](actions/list-webhook-message-kinds.md) | GET | Retrieves message webhook kinds from MailoPost. |

