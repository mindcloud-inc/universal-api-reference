# <img src="https://images.mindcloud.co/apps/icons/sign-well_1773341791294.png" alt="SignWell logo" width="28" height="28"> SignWell: Universal API

Send, sign, and manage documents and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signWell/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signwell.com
- **Vendor API docs:** https://developers.signwell.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credentials](actions/get-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Bulk Send

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Send](actions/create-bulk-send.md) | POST | Creates a new bulk send in SignWell. |
| [Get Bulk Send](actions/get-bulk-send.md) | GET | Retrieves details for a bulk send in SignWell. |
| [Get Bulk Send CSV Template](actions/get-bulk-send-csv-template.md) | GET | Retrieves a bulk send CSV template from SignWell. |
| [Get Bulk Send Documents](actions/get-bulk-send-documents.md) | GET | Retrieves documents for a bulk send in SignWell. |
| [List Bulk Sendings](actions/list-bulk-sendings.md) | GET | Lists bulk sends available in SignWell. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Completed PDF](actions/completed-pdf.md) | GET | Retrieves a completed document PDF from SignWell. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in SignWell. |
| [Create Document from Template](actions/create-document-from-template.md) | POST | Creates a new document from a template in SignWell. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from SignWell. |
| [Get Document](actions/get-document.md) | GET | Retrieves document details and recipients from SignWell. |
| [Send Reminder](actions/send-reminder.md) | POST | Sends a reminder for an unsigned document in SignWell. |
| [Update and Send Document](actions/update-and-send-document.md) | PUT | Updates and sends a draft document in SignWell. |
| [Update Recipients](actions/update-recipients.md) | PUT | Updates recipients on a sent document in SignWell. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Credentials](actions/get-credentials.md) | GET | Retrieves account and user details from SignWell. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in SignWell. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from SignWell. |
| [Get Template](actions/get-template.md) | GET | Retrieves template details and fields from SignWell. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in SignWell. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook subscription in SignWell. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook subscription from SignWell. |
| [List Webhooks](actions/list-webhooks.md) | GET | Lists webhook subscriptions configured in SignWell. |

