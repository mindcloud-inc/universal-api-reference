# <img src="https://images.mindcloud.co/apps/icons/stiply_1774377142025.png" alt="Stiply logo" width="28" height="28"> Stiply: Universal API

Stiply is a digital signing platform for sending, tracking, and managing legally valid sign requests and related signer artifacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stiply/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.stiply.nl/
- **Vendor API docs:** https://app.stiply.nl/api-documentation/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sign Requests](actions/list-sign-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Sign Request Documents](actions/list-sign-request-documents.md) | GET | Retrieves documents for a Stiply sign request. |

### Document File

| Action | Method | Description |
| --- | --- | --- |
| [Download Sign Request Document](actions/download-sign-request-document.md) | GET | Downloads a Stiply sign request document as a PDF. |

### Proof Document

| Action | Method | Description |
| --- | --- | --- |
| [Download Proof Document](actions/download-proof-document.md) | GET | Downloads the proof document for a completed Stiply sign request. |

### Sign Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Sign Request](actions/cancel-sign-request.md) | PUT | Cancels an existing Stiply sign request. |
| [Delete Sign Request](actions/delete-sign-request.md) | DELETE | Deletes an existing sign request from Stiply. |
| [Extend Sign Request Term](actions/extend-sign-request-term.md) | PUT | Extends the term of a Stiply sign request. |
| [Get Sign Request](actions/get-sign-request.md) | GET | Retrieves a sign request from Stiply by ID. |
| [Get Sign Request by External Key](actions/get-sign-request-by-external-key.md) | GET | Retrieves a Stiply sign request by external key. |
| [Get Sign Request by Key](actions/get-sign-request-by-key.md) | GET | Retrieves a Stiply sign request by key. |
| [List Sign Requests](actions/list-sign-requests.md) | GET | Retrieves sign requests available in Stiply. |
| [Send Sign Request](actions/send-sign-request.md) | POST | Creates and sends a new sign request in Stiply. |
| [Send Sign Request Reminder](actions/send-sign-request-reminder.md) | PUT | Sends a reminder for a Stiply sign request. |

### Sign Request File Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Download Sign Request Files](actions/download-sign-request-files.md) | GET | Downloads Stiply sign request documents as a ZIP file. |

### Sign Request Progress

| Action | Method | Description |
| --- | --- | --- |
| [List Sign Request Progress](actions/list-sign-request-progress.md) | GET | Retrieves progress entries for a Stiply sign request. |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Get Sign Request Signer](actions/get-sign-request-signer.md) | GET | Retrieves a signer from a Stiply sign request. |
| [List Sign Request Signers](actions/list-sign-request-signers.md) | GET | Retrieves signers for a Stiply sign request. |

### Signer Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Signer Attachment](actions/get-signer-attachment.md) | GET | Retrieves a signer attachment from a Stiply sign request. |
| [List Signer Attachments](actions/list-signer-attachments.md) | GET | Retrieves signer attachments for a Stiply sign request. |

### Signer Attachment File

| Action | Method | Description |
| --- | --- | --- |
| [Download Signer Attachment](actions/download-signer-attachment.md) | GET | Downloads a signer attachment from a Stiply sign request. |

### Signer Attachment File Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Download Signer Attachments](actions/download-signer-attachments.md) | GET | Downloads all attachments uploaded by a Stiply signer. |

