# Modusign: Native API Reference

A consolidated summary of Modusign's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developers.modusign.co.kr/reference/api-reference
- **API base URL:** `https://api.modusign.co.kr`

## Authentication

### Basic Auth

Use your Modusign account email as the Username field and your Modusign API key as the Password field.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.modusign.co.kr/docs/mcp)

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `orderBy` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document Label](actions/add-document-label.md) | `POST /documents/:documentId/labels` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Cancel Signature Request](actions/cancel-signature-request.md) | `POST /documents/:documentId/cancel` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Create Embedded Draft](actions/create-embedded-draft.md) | `POST /embedded-drafts` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Create Embedded Draft from Template](actions/create-embedded-draft-from-template.md) | `POST /embedded-drafts/create-with-template` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Create Label](actions/create-label.md) | `POST /labels` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Create Signature Request](actions/create-signature-request.md) | `POST /documents` | [docs](https://developers.modusign.co.kr/reference/documentcontroller_create) |
| [Create Signature Request from Template](actions/create-signature-request-from-template.md) | `POST /documents/request-with-template` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://developers.modusign.co.kr/reference/templatecontroller_create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Delete Label](actions/delete-label.md) | `DELETE /labels/:labelId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Forward Completed Document](actions/forward-completed-document.md) | `POST /documents/:documentId/send-completed-document` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://developers.modusign.co.kr/reference/documentcontroller_getdocument) |
| [Get Embedded Document View URL](actions/get-embedded-document-view-url.md) | `GET /documents/:documentId/embedded-view` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Participant Security Link](actions/get-participant-security-link.md) | `GET /documents/:documentId/participants/:participantId/security-link` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Requester Fields](actions/get-requester-fields.md) | `GET /documents/:documentId/requester-fields` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscription` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Subscription Usage](actions/get-subscription-usage.md) | `GET /subscription/usage` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Template](actions/get-template.md) | `GET /templates/:templateId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Get Template Embedded View URL](actions/get-template-embedded-view-url.md) | `GET /templates/:templateId/embedded-view` | [docs](https://developers.modusign.co.kr/docs/%EC%9E%84%EB%B2%A0%EB%94%94%EB%93%9C-%ED%85%9C%ED%94%8C%EB%A6%BF-%EC%88%98%EC%A0%95) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Attachments](actions/list-attachments.md) | `GET /documents/:documentId/attachments` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Document Histories](actions/list-document-histories.md) | `GET /documents/:documentId/histories` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Participant Fields](actions/list-participant-fields.md) | `GET /documents/:documentId/participant-fields` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Merge Files](actions/merge-files.md) | `POST /files/merge` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Remove Document Label](actions/remove-document-label.md) | `DELETE /documents/:documentId/labels/:labelId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Request Signature Content Update](actions/request-signature-content-update.md) | `POST /documents/:documentId/request-correction` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Resend Signature Request Notification](actions/resend-signature-request-notification.md) | `POST /documents/:documentId/remind-signing` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Update Current Signing Turn Expiration](actions/update-current-signing-turn-expiration.md) | `PUT /documents/:documentId/change-signing-due` | [docs](https://developers.modusign.co.kr/reference/documentcontroller_changesigningdueofcurrentorder) |
| [Update Document Metadata](actions/update-document-metadata.md) | `PUT /documents/:documentId/metadatas` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Update Label](actions/update-label.md) | `PUT /labels/:labelId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhookId` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://developers.modusign.co.kr/reference/api-reference) |
