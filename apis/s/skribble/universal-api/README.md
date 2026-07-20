# <img src="https://images.mindcloud.co/apps/icons/images_1774977261828.png" alt="Skribble logo" width="28" height="28"> Skribble: Universal API

Skribble lets teams create, send, track, and manage e-signature workflows, documents, seals, reports, and callback-driven signing operations through the public API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/skribble/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.skribble.com/
- **Vendor API docs:** https://api-doc.skribble.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Signature Requests](actions/list-signature-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Authentication Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | POST | Creates an API access token in Skribble. |

### Document Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Page Preview](actions/get-document-page-preview.md) | GET | Retrieves a preview image for a document page in Skribble. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in Skribble from a PDF upload. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Skribble or removes your access. |
| [Download Document Content](actions/download-document-content.md) | GET | Retrieves a document's PDF content from Skribble. |
| [Get Document](actions/get-document.md) | GET | Retrieves document metadata from Skribble. |
| [List Documents](actions/list-documents.md) | GET | Retrieves accessible documents from Skribble. |

### Seals

| Action | Method | Description |
| --- | --- | --- |
| [Create Seal](actions/create-seal.md) | POST | Creates a sealed document in Skribble. |

### Send-to

| Action | Method | Description |
| --- | --- | --- |
| [Create Send-To](actions/create-send-to.md) | POST | Creates a Send-To signing request in Skribble. |
| [Delete Send-To](actions/delete-send-to.md) | DELETE | Deletes a Send-To request from Skribble. |
| [Download Send-To Document](actions/download-send-to-document.md) | GET | Retrieves the current document for a Send-To request in Skribble. |
| [Track Send-To Status](actions/track-send-to-status.md) | GET | Retrieves the status of a Send-To request in Skribble. |

### Signature Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Signature Activities](actions/list-signature-activities.md) | GET | Retrieves signature activities for a business from Skribble. |

### Signature Request Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Attachment](actions/add-signature-request-attachment.md) | POST | Adds an attachment to a signature request in Skribble. |
| [Download Signature Request Attachment](actions/download-signature-request-attachment.md) | GET | Retrieves an attachment from a signature request in Skribble. |
| [Remove Signature Request Attachment](actions/remove-signature-request-attachment.md) | DELETE | Removes an attachment from a signature request in Skribble. |

### Signature Request Callbacks

| Action | Method | Description |
| --- | --- | --- |
| [List Signature Request Callbacks](actions/list-signature-request-callbacks.md) | GET | Retrieves callbacks for a signature request in Skribble. |

### Signature Request Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Request Report](actions/get-signature-request-report.md) | GET | Retrieves a signature report for a Skribble signature request. |

### Signature Request Signers

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Signer](actions/add-signature-request-signer.md) | POST | Adds a signer to a signature request in Skribble. |
| [Remove Signature Request Signer](actions/remove-signature-request-signer.md) | DELETE | Removes a signer from a signature request in Skribble. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a signature request in Skribble. |
| [Delete Signature Request](actions/delete-signature-request.md) | DELETE | Deletes a signature request from Skribble or removes your access. |
| [Get Signature Request](actions/get-signature-request.md) | GET | Retrieves a signature request from Skribble by ID. |
| [Get Signature Requests By Bulk](actions/get-signature-requests-by-bulk.md) | GET | Retrieves multiple signature requests from Skribble by ID. |
| [List Signature Requests](actions/list-signature-requests.md) | GET | Retrieves signature requests from Skribble. |
| [Remind Signature Request Signers](actions/remind-signature-request-signers.md) | PUT | Sends reminders to open signers in a Skribble signature request. |
| [Update Signature Request Signers](actions/update-signature-request-signers.md) | PUT | Updates the signer list for a signature request in Skribble. |
| [Withdraw Signature Request](actions/withdraw-signature-request.md) | PUT | Withdraws a signature request in Skribble. |

### System Health

| Action | Method | Description |
| --- | --- | --- |
| [Get System Health](actions/get-system-health.md) | GET | Retrieves the Skribble system health status. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Signature Qualities](actions/get-user-signature-qualities.md) | GET | Retrieves simplified user signature qualities from Skribble. |
| [Get User Signature Qualities Detail](actions/get-user-signature-qualities-detail.md) | GET | Retrieves detailed user signature qualities from Skribble. |

