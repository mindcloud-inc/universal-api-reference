# <img src="https://images.mindcloud.co/apps/icons/bulk-sms-envelope-01-1_1777324483808.png" alt="BulkSMS logo" width="28" height="28"> BulkSMS: Universal API

BulkSMS.com provides a JSON REST API for sending and receiving SMS messages, managing message webhooks and blocked numbers, viewing account profile information, transferring credits, and preparing SMS attachment uploads.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bulkSMS/latest
- **Category:** Marketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bulksms.com/
- **Vendor API docs:** https://www.bulksms.com/developer/json/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Attachment Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment Upload URL](actions/create-attachment-upload-url.md) | POST | Creates a signed BulkSMS attachment upload URL. |

### Blocked Number

| Action | Method | Description |
| --- | --- | --- |
| [Create Blocked Numbers](actions/create-blocked-numbers.md) | POST | Creates blocked phone numbers in BulkSMS. |
| [List Blocked Numbers](actions/list-blocked-numbers.md) | GET | Retrieves blocked phone numbers from BulkSMS. |

### Credit Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Credits](actions/transfer-credits.md) | POST | Transfers credits to another BulkSMS account. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Related Messages](actions/list-related-messages.md) | GET | Retrieves received messages related to a sent BulkSMS message. |
| [Retrieve Messages](actions/retrieve-messages.md) | GET | Retrieves sent or received messages from BulkSMS. |
| [Send Messages](actions/send-messages.md) | POST | Sends one or more messages through BulkSMS. |
| [Show Message](actions/show-message.md) | GET | Retrieves a message from BulkSMS by ID. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your account profile from BulkSMS. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in BulkSMS. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from BulkSMS. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks configured for your BulkSMS account. |
| [Read Webhook](actions/read-webhook.md) | GET | Retrieves a webhook from BulkSMS by ID. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in BulkSMS. |

