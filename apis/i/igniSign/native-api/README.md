# IgniSign: Native API Reference

A consolidated summary of IgniSign's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://ignisign.io/docs/quick-start/backend-integration/REST_API_Integration
- **API base URL:** `https://api.ignisign.io`

## Authentication

### API Key

Use an IgniSign v2 API key. IgniSign expects Authorization: Bearer <api key>.

### Credentials

- **API Key:** `apiKey` · required
- **Application ID:** `appId` · required · Your IgniSign application ID.
- **Environment:** `appEnv` · required · The IgniSign application environment.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ignisign.io/docs/quick-start/backend-integration/REST_API_Integration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Document Authenticity](actions/check-document-authenticity.md) | `POST /v4/documents/:documentId/check-authenticity` | [docs](https://ignisign.io/docs/ignisign-api/documents/check-document-authenticity) |
| [Check Webhook Event Token](actions/check-webhook-event-token.md) | `POST /v4/tokens/webhook-verification/checking-consumption` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/check-a-webhook-event-token) |
| [Close Signature Request](actions/close-signature-request.md) | `POST /v4/signature-requests/:signatureRequestId/close` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/close-a-signature-request) |
| [Create Document](actions/create-document.md) | `POST /v4/applications/:appId/envs/:appEnv/init-documents` | [docs](https://ignisign.io/docs/ignisign-api/documents/create-a-document) |
| [Create Signature Request in One Call](actions/create-signature-request-in-one-call.md) | `POST /v4/signature-requests/one-call-sign` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/create-a-signature-request-in-one-call) |
| [Create Signer](actions/create-signer.md) | `POST /v4/applications/:appId/envs/:appEnv/signers` | [docs](https://ignisign.io/docs/ignisign-api/signers/create-a-signer) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /v4/applications/:appId/envs/:appEnv/webhooks` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/add-a-new-webhook-endpoint) |
| [Delete Document](actions/delete-document.md) | `DELETE /v4/documents/:documentId` | [docs](https://ignisign.io/docs/ignisign-api/documents/remove-a-document) |
| [Delete Document Content](actions/delete-document-content.md) | `DELETE /v4/documents/:documentId/content` | [docs](https://ignisign.io/docs/ignisign-api/documents/remove-document-content) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /v4/webhooks/:webhookId` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/remove-a-webhook-endpoint) |
| [Download Low-Level Signature Proof](actions/download-low-level-signature-proof.md) | `GET /v4/documents/:documentId/signatures/:signatureType/signers/:signerId` | [docs](https://ignisign.io/docs/ignisign-api/documents/download-low-level-signature-proof) |
| [Download Original Document](actions/download-original-document.md) | `GET /v4/documents/:documentId/file` | [docs](https://ignisign.io/docs/ignisign-api/documents/download-the-original-document) |
| [Download Signature by Type](actions/download-signature-by-type.md) | `GET /v4/documents/:documentId/signatures/:signatureType` | [docs](https://ignisign.io/docs/ignisign-api/documents/download-signature-by-type) |
| [Get Application Context](actions/get-application-context.md) | `GET /v4/applications/:appId/context` | [docs](https://ignisign.io/docs/ignisign-api/application-context) |
| [Get Document](actions/get-document.md) | `GET /v4/documents/:documentId` | [docs](https://ignisign.io/docs/ignisign-api/documents/get-document-information) |
| [Get Document Context](actions/get-document-context.md) | `GET /v4/documents/:documentId/context` | [docs](https://ignisign.io/docs/ignisign-api/documents/get-a-document-context) |
| [Get Signature Images](actions/get-signature-images.md) | `GET /v4/documents/:documentId/img-signatures` | [docs](https://ignisign.io/docs/ignisign-api/documents/get-signature-images-base64) |
| [Get Signature Request Context](actions/get-signature-request-context.md) | `GET /v4/signature-requests/:signatureRequestId/context` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/get-a-signature-request-context) |
| [Get Signer Details](actions/get-signer-details.md) | `GET /v4/applications/:appId/envs/:appEnv/signers/:signerId/details` | [docs](https://ignisign.io/docs/ignisign-api/signers/get-a-signer-with-details) |
| [Get Signer Input Constraints](actions/get-signer-input-constraints.md) | `GET /v4/applications/:appId/envs/:appEnv/signer-profiles/:signerProfileId/inputs-needed` | [docs](https://ignisign.io/docs/ignisign-api/signer-profiles/get-signer-input-constraints) |
| [Get Signer Profile](actions/get-signer-profile.md) | `GET /v4/applications/:appId/envs/:appEnv/signer-profiles/:signerProfileId` | [docs](https://ignisign.io/docs/ignisign-api/signer-profiles/get-a-signer-profile) |
| [Get Signer Summary](actions/get-signer-summary.md) | `GET /v4/applications/:appId/envs/:appEnv/signers/:signerId` | [docs](https://ignisign.io/docs/ignisign-api/signers/get-signer-summary) |
| [Get Webhook Event](actions/get-webhook-event.md) | `GET /v4/webhooks/:webhookId/events/:eventId` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/get-a-webhook-event) |
| [Initialize Signature Request](actions/initialize-signature-request.md) | `POST /v4/applications/:appId/envs/:appEnv/signature-requests` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/initialize-a-signature-request) |
| [List Signature Requests](actions/list-signature-requests.md) | `GET /v4/applications/:appId/envs/:appEnv/signature-requests` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/get-signature-requests-paginated) |
| [List Signer Profiles](actions/list-signer-profiles.md) | `GET /v4/applications/:appId/envs/:appEnv/signer-profiles` | [docs](https://ignisign.io/docs/ignisign-api/signer-profiles/get-signer-profiles) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /v4/applications/:appId/envs/:appEnv/webhooks` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/get-webhook-endpoints) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /v4/webhooks/:webhookId/events` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/get-webhook-events) |
| [Publish Signature Request](actions/publish-signature-request.md) | `POST /v4/signature-requests/:signatureRequestId/publish` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/publish-a-signature-request) |
| [Regenerate Signer Authentication Secret](actions/regenerate-signer-authentication-secret.md) | `PUT /v4/applications/:appId/envs/:appEnv/signers/:signerId/regenerate-auth-secret` | [docs](https://ignisign.io/docs/ignisign-api/signers/regenerate-signer-authentication-secret) |
| [Resend Webhook Event](actions/resend-webhook-event.md) | `POST /v4/webhooks/:webhookId/events/:eventId/resend` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/resend-a-webhook-event) |
| [Revoke Signer](actions/revoke-signer.md) | `DELETE /v4/applications/:appId/envs/:appEnv/signers/:signerId/revoke` | [docs](https://ignisign.io/docs/ignisign-api/signers/revoke-a-signer) |
| [Search Signers](actions/search-signers.md) | `GET /v4/applications/:appId/envs/:appEnv/signers-paginate` | [docs](https://ignisign.io/docs/ignisign-api/signers/search-signers-pagination) |
| [Search Signers by Filters](actions/search-signers-by-filters.md) | `POST /v4/applications/:appId/envs/:appEnv/signers-search` | [docs](https://ignisign.io/docs/ignisign-api/signers/search-signers) |
| [Update Document](actions/update-document.md) | `PUT /v4/documents/:documentId` | [docs](https://ignisign.io/docs/ignisign-api/documents/update-document-information) |
| [Update Signature Request](actions/update-signature-request.md) | `PUT /v4/signature-requests/:signatureRequestId` | [docs](https://ignisign.io/docs/ignisign-api/signature-requests/update-a-signature-request) |
| [Update Signer](actions/update-signer.md) | `PUT /v4/applications/:appId/envs/:appEnv/signers/:signerId` | [docs](https://ignisign.io/docs/ignisign-api/signers/update-a-signer) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PUT /v4/webhooks/:webhookId` | [docs](https://ignisign.io/docs/ignisign-api/webhooks/update-a-webhook-endpoint) |
| [Upload Document Content Data JSON](actions/upload-document-content-data-json.md) | `POST /v4/documents/:documentId/data-json-content` | [docs](https://ignisign.io/docs/ignisign-api/documents/provide-document-content-data-json) |
| [Upload Document Content File](actions/upload-document-content-file.md) | `POST /v4/documents/:documentId/file` | [docs](https://ignisign.io/docs/ignisign-api/documents/provide-document-content-file-or-pdf) |
| [Upload Private Document Content](actions/upload-private-document-content.md) | `POST /v4/documents/:documentId/private-content` | [docs](https://ignisign.io/docs/ignisign-api/documents/provide-document-content-private-file) |
