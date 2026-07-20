# <img src="https://images.mindcloud.co/apps/icons/paperless-icon_1775747354661.png" alt="Paperless logo" width="28" height="28"> Paperless: Universal API

Paperless lets you create, send, track, and manage digital documents, templates, submissions, blobs, and webhook subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paperless/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paperless.io
- **Vendor API docs:** https://developers.paperless.io/docs/api/f935d3abd73dd-getting-started-with-the-paperless-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Blob

| Action | Method | Description |
| --- | --- | --- |
| [Create Blob](actions/create-blob.md) | POST |  |
| [Create Blob For Attachment](actions/create-blob-for-attachment.md) | POST |  |
| [Create Blob For Image](actions/create-blob-for-image.md) | POST |  |
| [Create Blob For PDF](actions/create-blob-for-pdf.md) | POST |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Advanced Document](actions/create-advanced-document.md) | POST |  |
| [Create Document](actions/create-document.md) | POST |  |
| [Create Document From PDF](actions/create-document-from-pdf.md) | POST |  |
| [Create Document From Template](actions/create-document-from-template.md) | POST |  |
| [Create Document With Email Content](actions/create-document-with-email-content.md) | POST |  |
| [Create Document With Form Fields](actions/create-document-with-form-fields.md) | POST |  |
| [Create Document With Hidden Blocks](actions/create-document-with-hidden-blocks.md) | POST |  |
| [Create Document With Redirect URL](actions/create-document-with-redirect-url.md) | POST |  |
| [Create Document With Reminder Settings](actions/create-document-with-reminder-settings.md) | POST |  |
| [Create Document With Signature Fields](actions/create-document-with-signature-fields.md) | POST |  |
| [Create Document With Variables](actions/create-document-with-variables.md) | POST |  |
| [Create Document With Visible Blocks](actions/create-document-with-visible-blocks.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Set Document Email Content](actions/set-document-email-content.md) | PUT |  |
| [Update Document](actions/update-document.md) | PUT |  |
| [Update Document Block Visibility](actions/update-document-block-visibility.md) | PUT |  |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Submission](actions/get-submission.md) | GET |  |
| [List Submissions](actions/list-submissions.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Created Webhook](actions/create-document-created-webhook.md) | POST |  |
| [Create Document Updated Webhook](actions/create-document-updated-webhook.md) | POST |  |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Document Created Webhooks](actions/list-document-created-webhooks.md) | GET |  |
| [List Document Updated Webhooks](actions/list-document-updated-webhooks.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [List Webhooks By Event](actions/list-webhooks-by-event.md) | GET |  |
| [Update Document Created Webhook](actions/update-document-created-webhook.md) | PUT |  |
| [Update Document Updated Webhook](actions/update-document-updated-webhook.md) | PUT |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

