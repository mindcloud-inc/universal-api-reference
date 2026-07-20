# Yousign: Native API Reference

A consolidated summary of Yousign's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developers.yousign.com/reference
- **OpenAPI specification:** https://developers.yousign.com/openapi/public-api-v3.json
- **API base URL:** `https://api-sandbox.yousign.app/v3`

## Authentication

### API Key

Connect with a Yousign API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.yousign.com/docs/set-up-your-account)

## API conventions

The next-page cursor is read from `meta.next_cursor`.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Signature Request](actions/activate-signature-request.md) | `POST /signature_requests/:signatureRequestId/activate` | [docs](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-activate-1) |
| [Add Signature Request Document](actions/add-signature-request-document.md) | `POST /signature_requests/:signatureRequestId/documents` | [docs](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-documents-1) |
| [Add Signature Request Signer](actions/add-signature-request-signer.md) | `POST /signature_requests/:signatureRequestId/signers` | [docs](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-signers-1) |
| [Cancel Signature Request](actions/cancel-signature-request.md) | `POST /signature_requests/:signatureRequestId/cancel` | [docs](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-cancel-1) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.yousign.com/reference/post-contact-1) |
| [Create Label](actions/create-label.md) | `POST /labels` | [docs](https://developers.yousign.com/reference/post-labels) |
| [Create Signature Request](actions/create-signature-request.md) | `POST /signature_requests` | [docs](https://developers.yousign.com/reference/post-signature_requests-1) |
| [Download Signature Request Documents](actions/download-signature-request-documents.md) | `GET /signature_requests/:signatureRequestId/documents/download` | [docs](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-documents-download-1) |
| [Fetch Signature Request](actions/fetch-signature-request.md) | `GET /signature_requests/:signatureRequestId` | [docs](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-1) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://developers.yousign.com/reference/get-contacts-contactid-1) |
| [Get Default Workspace](actions/get-default-workspace.md) | `GET /workspaces/default` | [docs](https://developers.yousign.com/reference/get-workspaces-default-1) |
| [Get Label](actions/get-label.md) | `GET /labels/:labelId` | [docs](https://developers.yousign.com/reference/get-labels-id) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://developers.yousign.com/reference/get-users-userid-1) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.yousign.com/reference/get-contacts-1) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://developers.yousign.com/reference/get-labels) |
| [List Signature Request Documents](actions/list-signature-request-documents.md) | `GET /signature_requests/:signatureRequestId/documents` | [docs](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-documents-1) |
| [List Signature Request Signers](actions/list-signature-request-signers.md) | `GET /signature_requests/:signatureRequestId/signers` | [docs](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-signers-1) |
| [List Signature Requests](actions/list-signature-requests.md) | `GET /signature_requests` | [docs](https://developers.yousign.com/reference/get-signature_requests-1) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.yousign.com/reference/get-templates-1) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.yousign.com/reference/get-users-1) |
| [Send Signer Reminder](actions/send-signer-reminder.md) | `POST /signature_requests/:signatureRequestId/signers/:signerId/send_reminder` | [docs](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-signers-signerid-send_reminder-1) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:contactId` | [docs](https://developers.yousign.com/reference/patch-contacts-contactid-1) |
| [Update Signature Request](actions/update-signature-request.md) | `PATCH /signature_requests/:signatureRequestId` | [docs](https://developers.yousign.com/reference/patch-signature_requests-signaturerequestid-1) |
