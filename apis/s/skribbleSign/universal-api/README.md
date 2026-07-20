# <img src="https://images.mindcloud.co/apps/icons/favicon-api-doc-skribble-com-48x48_1777914561873.png" alt="Skribble Sign logo" width="28" height="28"> Skribble Sign: Universal API

Create, manage, send, track, and download Skribble documents, signature requests, seals, and Send-To signing links through the Skribble API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/skribbleSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.skribble.com/
- **Vendor API docs:** https://api-doc.skribble.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get System Health](actions/get-system-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-system-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Authentication Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | POST | Creates a bearer token in Skribble Sign. |

### Document Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Page Preview](actions/get-document-page-preview.md) | GET | Retrieves a document page preview from Skribble Sign. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Skribble Sign. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Skribble Sign. |
| [Download Document Content](actions/download-document-content.md) | GET | Retrieves document content from Skribble Sign. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Skribble Sign. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Skribble Sign. |

### Seals

| Action | Method | Description |
| --- | --- | --- |
| [Create Seal](actions/create-seal.md) | POST | Creates a new seal in Skribble Sign. |

### Send-to

| Action | Method | Description |
| --- | --- | --- |
| [Create Send-To](actions/create-send-to.md) | POST | Creates a new Send-To request in Skribble Sign. |
| [Delete Send-To](actions/delete-send-to.md) | DELETE | Deletes an existing Send-To request from Skribble Sign. |
| [Download Send-To Document](actions/download-send-to-document.md) | GET | Retrieves a Send-To document from Skribble Sign. |
| [Track Send-To Status](actions/track-send-to-status.md) | GET | Retrieves Send-To delivery status from Skribble Sign. |

### Signature Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Signature Activities](actions/list-signature-activities.md) | GET | Retrieves signature activities from Skribble Sign. |

### Signature Request Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Attachment](actions/add-signature-request-attachment.md) | POST | Adds an attachment to a signature request in Skribble Sign. |
| [Download Signature Request Attachment](actions/download-signature-request-attachment.md) | GET | Retrieves a signature request attachment from Skribble Sign. |
| [Remove Signature Request Attachment](actions/remove-signature-request-attachment.md) | DELETE | Deletes a signature request attachment from Skribble Sign. |

### Signature Request Callbacks

| Action | Method | Description |
| --- | --- | --- |
| [List Signature Request Callbacks](actions/list-signature-request-callbacks.md) | GET | Retrieves signature request callbacks from Skribble Sign. |

### Signature Request Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Request Report](actions/get-signature-request-report.md) | GET | Retrieves a signature request report from Skribble Sign. |

### Signature Request Signers

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Signer](actions/add-signature-request-signer.md) | POST | Adds a signer to a signature request in Skribble Sign. |
| [Remove Signature Request Signer](actions/remove-signature-request-signer.md) | DELETE | Deletes a signature request signer from Skribble Sign. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a new signature request in Skribble Sign. |
| [Delete Signature Request](actions/delete-signature-request.md) | DELETE | Deletes an existing signature request from Skribble Sign. |
| [Get Signature Request](actions/get-signature-request.md) | GET | Retrieves a signature request from Skribble Sign. |
| [Get Signature Requests By Bulk](actions/get-signature-requests-by-bulk.md) | GET | Retrieves signature requests by bulk ID in Skribble Sign. |
| [List Signature Requests](actions/list-signature-requests.md) | GET | Retrieves signature requests from Skribble Sign. |
| [Remind Signature Request Signers](actions/remind-signature-request-signers.md) | PUT | Sends reminder emails for signature request signers in Skribble Sign. |
| [Update Signature Request Signers](actions/update-signature-request-signers.md) | PUT | Updates signature request signers in Skribble Sign. |
| [Withdraw Signature Request](actions/withdraw-signature-request.md) | PUT | Withdraws a signature request in Skribble Sign. |

### System Health

| Action | Method | Description |
| --- | --- | --- |
| [Get System Health](actions/get-system-health.md) | GET | Retrieves system health from Skribble Sign. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Signature Qualities](actions/get-user-signature-qualities.md) | GET | Retrieves user signature qualities from Skribble Sign. |
| [Get User Signature Qualities Detail](actions/get-user-signature-qualities-detail.md) | GET | Retrieves detailed user signature qualities from Skribble Sign. |

