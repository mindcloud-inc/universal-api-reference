# <img src="https://images.mindcloud.co/apps/icons/ignisign-icon-square_1775662039114.png" alt="IgniSign logo" width="28" height="28"> IgniSign: Universal API

IgniSign is an e-signature platform for managing signers, documents, signature requests, webhooks, and application users over the IgniSign REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/igniSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ignisign.io
- **Vendor API docs:** https://ignisign.io/docs/quick-start/backend-integration/REST_API_Integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Application Context](actions/get-application-context.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Context](actions/get-application-context.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Check Document Authenticity](actions/check-document-authenticity.md) | GET |  |
| [Create Document](actions/create-document.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Delete Document Content](actions/delete-document-content.md) | DELETE |  |
| [Download Low-Level Signature Proof](actions/download-low-level-signature-proof.md) | GET |  |
| [Download Original Document](actions/download-original-document.md) | GET |  |
| [Download Signature by Type](actions/download-signature-by-type.md) | GET |  |
| [Get Document](actions/get-document.md) | GET |  |
| [Get Document Context](actions/get-document-context.md) | GET |  |
| [Get Signature Images](actions/get-signature-images.md) | GET |  |
| [Update Document](actions/update-document.md) | PUT |  |
| [Upload Document Content Data JSON](actions/upload-document-content-data-json.md) | PUT |  |
| [Upload Document Content File](actions/upload-document-content-file.md) | PUT |  |
| [Upload Private Document Content](actions/upload-private-document-content.md) | PUT |  |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Close Signature Request](actions/close-signature-request.md) | PUT |  |
| [Create Signature Request in One Call](actions/create-signature-request-in-one-call.md) | POST |  |
| [Get Signature Request Context](actions/get-signature-request-context.md) | GET |  |
| [Initialize Signature Request](actions/initialize-signature-request.md) | POST |  |
| [List Signature Requests](actions/list-signature-requests.md) | GET |  |
| [Publish Signature Request](actions/publish-signature-request.md) | PUT |  |
| [Update Signature Request](actions/update-signature-request.md) | PUT |  |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Create Signer](actions/create-signer.md) | POST |  |
| [Get Signer Details](actions/get-signer-details.md) | GET |  |
| [Get Signer Summary](actions/get-signer-summary.md) | GET |  |
| [Revoke Signer](actions/revoke-signer.md) | DELETE |  |
| [Search Signers](actions/search-signers.md) | GET |  |
| [Search Signers by Filters](actions/search-signers-by-filters.md) | GET |  |
| [Update Signer](actions/update-signer.md) | PUT |  |

### Signer Input Constraint

| Action | Method | Description |
| --- | --- | --- |
| [Get Signer Input Constraints](actions/get-signer-input-constraints.md) | GET |  |

### Signer Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Signer Profile](actions/get-signer-profile.md) | GET |  |
| [List Signer Profiles](actions/list-signer-profiles.md) | GET |  |

### Signer Secret

| Action | Method | Description |
| --- | --- | --- |
| [Regenerate Signer Authentication Secret](actions/regenerate-signer-authentication-secret.md) | PUT |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST |  |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE |  |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET |  |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT |  |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [Check Webhook Event Token](actions/check-webhook-event-token.md) | GET |  |
| [Get Webhook Event](actions/get-webhook-event.md) | GET |  |
| [List Webhook Events](actions/list-webhook-events.md) | GET |  |
| [Resend Webhook Event](actions/resend-webhook-event.md) | PUT |  |

