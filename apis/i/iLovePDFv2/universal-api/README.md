# <img src="https://images.mindcloud.co/apps/icons/favicon-www-iloveapi-com-48x48_1777482995278.png" alt="iLovePDFv2 logo" width="28" height="28"> iLovePDFv2: Universal API

PDF, image, and e-signature automation for iLoveAPI/iLovePDF tasks, including task creation, task history, and signature request management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iLovePDFv2/latest
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.iloveapi.com
- **Vendor API docs:** https://www.iloveapi.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Token](actions/get-auth-token.md) | GET | Retrieves an auth token from iLovePDFv2. |

### Processed File

| Action | Method | Description |
| --- | --- | --- |
| [Download Task Result](actions/download-task-result.md) | GET | Downloads output files for an iLovePDFv2 task. |

### Signature Receiver

| Action | Method | Description |
| --- | --- | --- |
| [Get Receiver Info](actions/get-receiver-info.md) | GET | Retrieves a signature receiver from iLovePDFv2 by receiver token. |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature Status](actions/get-signature-status.md) | GET | Retrieves a signature request from iLovePDFv2 by requester token. |
| [Increase Signature Expiration Days](actions/increase-signature-expiration-days.md) | PUT |  |
| [List Signatures](actions/list-signatures.md) | GET | Lists signature requests in iLovePDFv2. |
| [Void Signature](actions/void-signature.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Connect Task](actions/connect-task.md) | POST | Creates a follow-up task from an iLovePDFv2 task. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an iLovePDFv2 task and its files. |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Process Task](actions/process-task.md) | POST | Processes uploaded files for an iLovePDFv2 task. |
| [Start Compress PDF Task](actions/start-compress-task.md) | POST | Starts a PDF compression task in iLovePDFv2. |
| [Start Compress Image Task](actions/start-compressimage-task.md) | POST | Starts an image compression task in iLovePDFv2. |
| [Start Convert Image Task](actions/start-convertimage-task.md) | POST | Starts an image conversion task in iLovePDFv2. |
| [Start Crop Image Task](actions/start-cropimage-task.md) | POST | Starts an image cropping task in iLovePDFv2. |
| [Start Edit PDF Task](actions/start-editpdf-task.md) | POST | Starts a PDF editing task in iLovePDFv2. |
| [Start Extract PDF Task](actions/start-extract-task.md) | POST | Starts a PDF extraction task in iLovePDFv2. |
| [Start HTML to PDF Task](actions/start-htmlpdf-task.md) | POST | Starts an HTML to PDF task in iLovePDFv2. |
| [Start Image to PDF Task](actions/start-imagepdf-task.md) | POST | Starts an image to PDF task in iLovePDFv2. |
| [Start Merge PDF Task](actions/start-merge-task.md) | POST | Starts a PDF merge task in iLovePDFv2. |
| [Start Office to PDF Task](actions/start-officepdf-task.md) | POST | Starts an Office to PDF task in iLovePDFv2. |
| [Start Add Page Numbers Task](actions/start-pagenumber-task.md) | POST | Starts a PDF page numbering task in iLovePDFv2. |
| [Start PDF to PDF/A Task](actions/start-pdfa-task.md) | POST | Starts a PDF to PDF/A task in iLovePDFv2. |
| [Start PDF to JPG Task](actions/start-pdfjpg-task.md) | POST | Starts a PDF to JPG task in iLovePDFv2. |
| [Start OCR PDF Task](actions/start-pdfocr-task.md) | POST | Starts a PDF OCR task in iLovePDFv2. |
| [Start Protect PDF Task](actions/start-protect-task.md) | POST | Starts a PDF protection task in iLovePDFv2. |
| [Start Remove Image Background Task](actions/start-removebackgroundimage-task.md) | POST | Starts an image background removal task in iLovePDFv2. |
| [Start Repair PDF Task](actions/start-repair-task.md) | POST | Starts a PDF repair task in iLovePDFv2. |
| [Start Repair Image Task](actions/start-repairimage-task.md) | POST | Starts an image repair task in iLovePDFv2. |
| [Start Resize Image Task](actions/start-resizeimage-task.md) | POST | Starts an image resize task in iLovePDFv2. |
| [Start Rotate PDF Task](actions/start-rotate-task.md) | POST | Starts a PDF rotation task in iLovePDFv2. |
| [Start Rotate Image Task](actions/start-rotateimage-task.md) | POST | Starts an image rotation task in iLovePDFv2. |
| [Start Split PDF Task](actions/start-split-task.md) | POST | Starts a PDF split task in iLovePDFv2. |
| [Start Unlock PDF Task](actions/start-unlock-task.md) | POST | Starts a PDF unlock task in iLovePDFv2. |
| [Start Upscale Image Task](actions/start-upscaleimage-task.md) | POST | Starts an image upscaling task in iLovePDFv2. |
| [Start Validate PDF/A Task](actions/start-validatepdfa-task.md) | POST | Starts a PDF/A validation task in iLovePDFv2. |
| [Start Add PDF Watermark Task](actions/start-watermark-task.md) | POST | Starts a PDF watermark task in iLovePDFv2. |
| [Start Add Image Watermark Task](actions/start-watermarkimage-task.md) | POST | Starts an image watermark task in iLovePDFv2. |

### Uploaded File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File From URL](actions/upload-file-from-url.md) | POST | Uploads a file to an iLovePDFv2 task from a URL. |

