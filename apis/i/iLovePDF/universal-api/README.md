# <img src="https://images.mindcloud.co/apps/icons/i-love-pdf_1773862528157.png" alt="iLovePDF logo" width="28" height="28"> iLovePDF: Universal API

Process PDFs, extract content, and manage digital signature requests

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iLovePDF/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ilovepdf.com
- **Vendor API docs:** https://www.iloveapi.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Audit](actions/download-audit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/download-audit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Audit](actions/download-audit.md) | GET | Retrieves an audit file from iLovePDF. |
| [Download Original Files](actions/download-original-files.md) | GET | Retrieves original files from an iLovePDF signature request. |
| [Download Output Files](actions/download-output-files.md) | GET | Retrieves processed output files from iLovePDF. |
| [Download Signed Files](actions/download-signed-files.md) | GET | Retrieves signed files from an iLovePDF signature request. |
| [Remove Uploaded File](actions/remove-uploaded-file.md) | DELETE | Deletes an uploaded file from iLovePDF. |
| [Upload File From URL](actions/upload-file-from-url.md) | POST | Uploads a file from a URL to iLovePDF. |
| [Upload Local File](actions/upload-local-file.md) | POST | Uploads a local file to iLovePDF. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a signature request in iLovePDF. |
| [Fix Receiver Email](actions/fix-receiver-email.md) | PUT | Updates a signer email in an iLovePDF signature request. |
| [Fix Signer Phone](actions/fix-signer-phone.md) | PUT | Updates a signer phone number in an iLovePDF signature request. |
| [Get Receiver Info](actions/get-receiver-info.md) | GET | Retrieves signer info from an iLovePDF signature request. |
| [Get Signature Status](actions/get-signature-status.md) | GET | Retrieves a signature request from iLovePDF. |
| [Increase Expiration Days](actions/increase-expiration-days.md) | PUT | Extends signature request expiration in iLovePDF. |
| [List Signatures](actions/list-signatures.md) | GET | Retrieves signature requests from iLovePDF. |
| [Send Reminders](actions/send-reminders.md) | PUT | Sends signature reminders in iLovePDF. |
| [Void Signature](actions/void-signature.md) | PUT | Voids a signature request in iLovePDF. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Compress PDF](actions/compress-pdf.md) | POST | Creates a compressed PDF in iLovePDF. |
| [Connect Task](actions/connect-task.md) | POST | Connects an existing task to a follow-up task in iLovePDF. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from iLovePDF. |
| [Edit PDF](actions/edit-pdf.md) | POST | Edits a PDF in iLovePDF. |
| [Extract PDF](actions/extract-pdf.md) | POST | Extracts pages from a PDF in iLovePDF. |
| [Get Server and Task ID](actions/get-server-and-task-id.md) | POST | Creates a task and server assignment in iLovePDF. |
| [Get Signature Server and Task ID](actions/get-signature-server-and-task-id.md) | POST | Creates a signature task and server assignment in iLovePDF. |
| [HTML to PDF](actions/html-to-pdf.md) | POST | Converts HTML to PDF in iLovePDF. |
| [JPG to PDF](actions/jpg-to-pdf.md) | POST | Creates a PDF from JPG files in iLovePDF. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from iLovePDF. |
| [Merge PDF](actions/merge-pdf.md) | POST | Creates a merged PDF in iLovePDF. |
| [Office to PDF](actions/office-to-pdf.md) | POST | Converts Office files to PDF in iLovePDF. |
| [Page Numbers](actions/page-numbers.md) | POST | Adds page numbers to a PDF in iLovePDF. |
| [PDF OCR](actions/pdf-ocr.md) | POST | Creates OCR output from a PDF in iLovePDF. |
| [PDF to JPG](actions/pdf-to-jpg.md) | POST | Creates JPG files from a PDF in iLovePDF. |
| [PDF to PDF/A](actions/pdf-to-pdfa.md) | POST | Converts a PDF to PDF/A in iLovePDF. |
| [Process Files](actions/process-files.md) | POST | Processes uploaded files in iLovePDF. |
| [Protect PDF](actions/protect-pdf.md) | POST | Protects a PDF in iLovePDF. |
| [Repair PDF](actions/repair-pdf.md) | POST | Repairs a PDF in iLovePDF. |
| [Rotate PDF](actions/rotate-pdf.md) | POST | Rotates PDF pages in iLovePDF. |
| [Split PDF](actions/split-pdf.md) | POST | Creates split PDF files in iLovePDF. |
| [Unlock PDF](actions/unlock-pdf.md) | POST | Creates an unlocked PDF in iLovePDF. |
| [Validate PDF/A](actions/validate-pdfa.md) | POST | Validates a PDF/A file in iLovePDF. |
| [Watermark PDF](actions/watermark-pdf.md) | POST | Adds a watermark to a PDF in iLovePDF. |

