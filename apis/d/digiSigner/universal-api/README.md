# <img src="https://images.mindcloud.co/apps/icons/digi-signer_1776701165558.png" alt="DigiSigner logo" width="28" height="28"> DigiSigner: Universal API

Send, sign, and manage eSignature documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digiSigner/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digisigner.com
- **Vendor API docs:** https://www.digisigner.com/esignature-api/esignature-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Document Fields](actions/get-document-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from DigiSigner by ID. |
| [Download Document](actions/download-document.md) | GET | Downloads a document from DigiSigner by ID. |
| [Upload Document](actions/upload-document.md) | POST | Uploads a new document to DigiSigner. |

### Document Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Document Attachment](actions/download-document-attachment.md) | GET | Downloads a document attachment from DigiSigner by field ID. |

### Document Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Fields](actions/get-document-fields.md) | GET | Retrieves document fields from DigiSigner by document ID. |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Request Status](actions/get-signature-request-status.md) | GET | Retrieves a DigiSigner signature request by ID. |
| [Send Signature Request](actions/send-signature-request.md) | POST | Creates a signature request in DigiSigner. |

