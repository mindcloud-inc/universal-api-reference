# Skribble Sign: Native API Reference

A consolidated summary of Skribble Sign's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api-doc.skribble.com/
- **API base URL:** `https://api.skribble.com`

## Authentication

### Skribble API Login

### Credentials

- **Username:** `username` · required · Skribble API username. Demo users usually start with api_demo.
- **API Key:** `apiKey` · required · Skribble API key used together with the API username to mint a short-lived bearer token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.response>
```

[Official authentication documentation](https://api-doc.skribble.com/#d0385a4a-edea-4498-9f49-dde78c28cf50)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/plain, */*` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Signature Request Attachment](actions/add-signature-request-attachment.md) | `POST /v2/signature-requests/:signatureRequestId/attachments` | [docs](https://api-doc.skribble.com/#8f8b71fd-3a23-4e88-b770-ea83090e41f2) |
| [Add Signature Request Signer](actions/add-signature-request-signer.md) | `POST /v2/signature-requests/:signatureRequestId/signatures` | [docs](https://api-doc.skribble.com/#20c99183-10a0-4142-a763-b3b91d4854db) |
| [Create Document](actions/create-document.md) | `POST /v2/documents` | [docs](https://api-doc.skribble.com/#9cf195d0-bec5-4037-899d-1919b003b347) |
| [Create Seal](actions/create-seal.md) | `POST /v2/seal` | [docs](https://api-doc.skribble.com/#72ed542c-7e2a-4140-ae03-27780b78acf7) |
| [Create Send-To](actions/create-send-to.md) | `POST /v2/sendto` | [docs](https://api-doc.skribble.com/#1b649c7f-5bfa-4c8c-b9db-5eb7a71bdd6c) |
| [Create Signature Request](actions/create-signature-request.md) | `POST /v2/signature-requests` | [docs](https://api-doc.skribble.com/#4dd248c5-1700-4812-977c-445d492fba5e) |
| [Delete Document](actions/delete-document.md) | `DELETE /v2/documents/:documentId` | [docs](https://api-doc.skribble.com/#294578e1-93f2-4d41-bc55-2850bfd7c4c1) |
| [Delete Send-To](actions/delete-send-to.md) | `DELETE /v2/sendto/:sendToId` | [docs](https://api-doc.skribble.com/#59ff33dd-6661-49eb-b4c6-b98918efeb70) |
| [Delete Signature Request](actions/delete-signature-request.md) | `DELETE /v2/signature-requests/:signatureRequestId` | [docs](https://api-doc.skribble.com/#beedd756-f48a-4a59-920a-09cad1226c0a) |
| [Download Document Content](actions/download-document-content.md) | `GET /v2/documents/:documentId/content` | [docs](https://api-doc.skribble.com/#c11a7ec0-8251-456c-9ac8-e2b89b505fc3) |
| [Download Send-To Document](actions/download-send-to-document.md) | `GET /v2/sendto/:sendToId/download` | [docs](https://api-doc.skribble.com/#2aded87e-41cf-4e07-ad94-e75d7eae7f42) |
| [Download Signature Request Attachment](actions/download-signature-request-attachment.md) | `GET /v2/signature-requests/:signatureRequestId/attachments/:attachmentId/content` | [docs](https://api-doc.skribble.com/#04a7353f-8a42-4645-a9f6-90723400fd0e) |
| [Get Document](actions/get-document.md) | `GET /v2/documents/:documentId` | [docs](https://api-doc.skribble.com/#7178df86-708e-44ca-a064-cf4f049a291d) |
| [Get Document Page Preview](actions/get-document-page-preview.md) | `GET /v2/documents/:documentId/pages/:pageId` | [docs](https://api-doc.skribble.com/#f168728b-dccb-4c6c-ad22-8120ab2cddff) |
| [Get Signature Request](actions/get-signature-request.md) | `GET /v2/signature-requests/:signatureRequestId` | [docs](https://api-doc.skribble.com/#874d9e77-5bb4-4381-9252-925f538c5dbc) |
| [Get Signature Request Report](actions/get-signature-request-report.md) | `GET /v2/signature-requests/:signatureRequestId/report` | [docs](https://api-doc.skribble.com/#cd6deb59-5d9f-47e7-9bf7-99b3bdfed8ed) |
| [Get Signature Requests By Bulk](actions/get-signature-requests-by-bulk.md) | `POST /v2/signature-requests/bulk` | [docs](https://api-doc.skribble.com/#68a481be-fdb1-4474-8bd5-29df60302b76) |
| [Get System Health](actions/get-system-health.md) | `GET /management/health` | [docs](https://api-doc.skribble.com/#75d22845-3e7f-4bb6-af19-91766da7b3a9) |
| [Get User Signature Qualities](actions/get-user-signature-qualities.md) | `GET /v2/user/signature-qualities` | [docs](https://api-doc.skribble.com/#b4605fb0-ef85-4d0f-9bd3-2a6db9b0f2e0) |
| [Get User Signature Qualities Detail](actions/get-user-signature-qualities-detail.md) | `GET /v2/user/signature-qualities-detail` | [docs](https://api-doc.skribble.com/#8de1cfa7-e5ed-423a-8c5d-40ba3efc5f2b) |
| [List Documents](actions/list-documents.md) | `GET /v2/documents` | [docs](https://api-doc.skribble.com/#97e9da9c-9f86-484a-89e3-b968394d334d) |
| [List Signature Activities](actions/list-signature-activities.md) | `GET /v2/activities/signatures` | [docs](https://api-doc.skribble.com/#f2f445ee-c62b-4b0f-99ab-63ea72c2ba16) |
| [List Signature Request Callbacks](actions/list-signature-request-callbacks.md) | `GET /v2/signature-requests/:signatureRequestId/callbacks` | [docs](https://api-doc.skribble.com/#c74befb3-5fbd-42ec-b23b-107faf7d0a74) |
| [List Signature Requests](actions/list-signature-requests.md) | `GET /v2/signature-requests` | [docs](https://api-doc.skribble.com/#c5136386-30d1-46ff-a74b-ba35f752e7d7) |
| [Login](actions/login.md) | `POST /v2/access/login` | [docs](https://api-doc.skribble.com/#4faa3dbc-6b67-450c-a592-d93add26d56a) |
| [Remind Signature Request Signers](actions/remind-signature-request-signers.md) | `POST /v2/signature-requests/:signatureRequestId/remind` | [docs](https://api-doc.skribble.com/#d70ed206-dc9f-42d2-b864-a10f2572fbac) |
| [Remove Signature Request Attachment](actions/remove-signature-request-attachment.md) | `DELETE /v2/signature-requests/:signatureRequestId/attachments/:attachmentId` | [docs](https://api-doc.skribble.com/#de1edd9b-bef3-4c59-a3c0-744421b1ae61) |
| [Remove Signature Request Signer](actions/remove-signature-request-signer.md) | `DELETE /v2/signature-requests/:signatureRequestId/signatures/:signatureId` | [docs](https://api-doc.skribble.com/#f3170c1e-1ebe-4b52-ad25-bb4fac976f3d) |
| [Track Send-To Status](actions/track-send-to-status.md) | `GET /v2/sendto/:sendToId/track` | [docs](https://api-doc.skribble.com/#9be42ece-fe87-4132-8d73-2c964044dc36) |
| [Update Signature Request Signers](actions/update-signature-request-signers.md) | `PUT /v2/signature-requests` | [docs](https://api-doc.skribble.com/#c1a29021-bb26-40af-9bd2-c4a774e4a18d) |
| [Withdraw Signature Request](actions/withdraw-signature-request.md) | `POST /v2/signature-requests/:signatureRequestId/withdraw` | [docs](https://api-doc.skribble.com/#65b879fe-43ad-40bf-98a0-fe3323fcbe56) |
