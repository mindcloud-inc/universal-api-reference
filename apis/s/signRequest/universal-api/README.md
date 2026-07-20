# <img src="https://images.mindcloud.co/apps/icons/sign-request_1773340060722.png" alt="SignRequest logo" width="28" height="28"> SignRequest: Universal API

Send, sign, and manage documents with SignRequest

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signRequest/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://signrequest.com
- **Vendor API docs:** https://signrequest.com/api/v1/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List SignRequests](actions/list-sign-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Search Documents](actions/search-documents.md) | GET |  |

### Document Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Attachment](actions/create-document-attachment.md) | POST |  |
| [Get Document Attachment](actions/get-document-attachment.md) | GET |  |
| [List Document Attachments](actions/list-document-attachments.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |

### Signrequest

| Action | Method | Description |
| --- | --- | --- |
| [Cancel SignRequest](actions/cancel-sign-request.md) | PUT |  |
| [Create SignRequest](actions/create-sign-request.md) | POST |  |
| [Forward SignRequest](actions/forward-sign-request.md) | PUT |  |
| [Get SignRequest](actions/get-sign-request.md) | GET |  |
| [List SignRequests](actions/list-sign-requests.md) | GET |  |
| [Quick Create SignRequest](actions/quick-create-sign-request.md) | POST |  |
| [Resend SignRequest](actions/resend-sign-request.md) | PUT |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

