# <img src="https://images.mindcloud.co/apps/icons/images-25_1774890242238.png" alt="Modusign logo" width="28" height="28"> Modusign: Universal API

Modusign is an e-signature API for managing signature requests, templates, embedded signing flows, labels, webhooks, subscriptions, and file uploads over HTTP Basic auth.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/modusign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.modusign.co.kr
- **Vendor API docs:** https://developers.modusign.co.kr/reference/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments for a document from Modusign. |
| [Merge Files](actions/merge-files.md) | POST | Merges uploaded files into one document file in Modusign. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Modusign. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Document Label](actions/add-document-label.md) | PUT | Adds a label to a document in Modusign. |
| [Cancel Signature Request](actions/cancel-signature-request.md) | PUT | Cancels an existing signature request in Modusign. |
| [Create Embedded Draft](actions/create-embedded-draft.md) | POST | Creates a new embedded draft in Modusign. |
| [Create Embedded Draft from Template](actions/create-embedded-draft-from-template.md) | POST | Creates an embedded draft from a template in Modusign. |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a new signature request in Modusign. |
| [Create Signature Request from Template](actions/create-signature-request-from-template.md) | POST | Creates a signature request from a template in Modusign. |
| [Forward Completed Document](actions/forward-completed-document.md) | PUT | Forwards a completed document link from Modusign. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Modusign. |
| [Get Embedded Document View URL](actions/get-embedded-document-view-url.md) | GET | Retrieves an embedded document view URL from Modusign. |
| [Get Participant Security Link](actions/get-participant-security-link.md) | GET | Retrieves a participant security link from Modusign. |
| [Get Requester Fields](actions/get-requester-fields.md) | GET | Retrieves requester input fields from Modusign. |
| [List Document Histories](actions/list-document-histories.md) | GET | Retrieves document history entries from Modusign. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from Modusign. |
| [List Participant Fields](actions/list-participant-fields.md) | GET | Retrieves participant input fields from Modusign. |
| [Remove Document Label](actions/remove-document-label.md) | PUT | Removes a label from a document in Modusign. |
| [Request Signature Content Update](actions/request-signature-content-update.md) | PUT | Requests a signature content correction in Modusign. |
| [Resend Signature Request Notification](actions/resend-signature-request-notification.md) | PUT | Resends a signing notification in Modusign. |
| [Update Current Signing Turn Expiration](actions/update-current-signing-turn-expiration.md) | PUT | Updates the current signing turn expiration in Modusign. |
| [Update Document Metadata](actions/update-document-metadata.md) | PUT | Replaces existing document metadata in Modusign. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves current subscription details from Modusign. |
| [Get Subscription Usage](actions/get-subscription-usage.md) | GET | Retrieves subscription usage from Modusign using UTC dates. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Modusign. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from Modusign. |
| [List Labels](actions/list-labels.md) | GET | Retrieves a list of labels from Modusign. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in Modusign. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Modusign. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Modusign. |
| [Get Template Embedded View URL](actions/get-template-embedded-view-url.md) | GET | Retrieves an embedded template view URL from Modusign. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from Modusign. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Modusign. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Modusign. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Modusign. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Modusign. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Modusign. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Modusign. |

