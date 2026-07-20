# iLovePDFv2: Native API Reference

A consolidated summary of iLovePDFv2's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://www.iloveapi.com/docs/api-reference
- **API base URL:** `https://api.ilovepdf.com/v1`

## Authentication

### iLoveAPI keys

Custom iLoveAPI authentication. The public key is exchanged for a short-lived JWT token and the secret key is retained for server-side task-history endpoints.

### Credentials

- **Project public key:** `publicKey` · required · Project public key from the iLoveAPI developer console.
- **Project secret key:** `secretKey` · required · Project secret key from the iLoveAPI developer console. Stored encrypted and used only server-side.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://www.iloveapi.com/docs/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connect Task](actions/connect-task.md) | `POST https://:server/v1/task/next` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Delete Task](actions/delete-task.md) | `DELETE https://:server/v1/task/:task` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Download Task Result](actions/download-task-result.md) | `GET https://:server/v1/download/:task` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Get Auth Token](actions/get-auth-token.md) | `POST /auth` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Get Receiver Info](actions/get-receiver-info.md) | `GET /signature/receiver/info/:receiver_token_requester` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Get Signature Status](actions/get-signature-status.md) | `GET /signature/requesterview/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Increase Signature Expiration Days](actions/increase-signature-expiration-days.md) | `POST /signature/increase-expiration-days/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [List Signatures](actions/list-signatures.md) | `GET /signature/list` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [List Tasks](actions/list-tasks.md) | `GET /task` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Process Task](actions/process-task.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Compress PDF Task](actions/start-compress-task.md) | `GET /start/compress/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Compress Image Task](actions/start-compressimage-task.md) | `GET https://api.iloveimg.com/v1/start/compressimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Convert Image Task](actions/start-convertimage-task.md) | `GET https://api.iloveimg.com/v1/start/convertimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Crop Image Task](actions/start-cropimage-task.md) | `GET https://api.iloveimg.com/v1/start/cropimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Edit PDF Task](actions/start-editpdf-task.md) | `GET /start/editpdf/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Extract PDF Task](actions/start-extract-task.md) | `GET /start/extract/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start HTML to PDF Task](actions/start-htmlpdf-task.md) | `GET /start/htmlpdf` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Image to PDF Task](actions/start-imagepdf-task.md) | `GET /start/imagepdf/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Merge PDF Task](actions/start-merge-task.md) | `GET /start/merge/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Office to PDF Task](actions/start-officepdf-task.md) | `GET /start/officepdf/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Add Page Numbers Task](actions/start-pagenumber-task.md) | `GET /start/pagenumber/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start PDF to PDF/A Task](actions/start-pdfa-task.md) | `GET /start/pdfa/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start PDF to JPG Task](actions/start-pdfjpg-task.md) | `GET /start/pdfjpg/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start OCR PDF Task](actions/start-pdfocr-task.md) | `GET /start/pdfocr/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Protect PDF Task](actions/start-protect-task.md) | `GET /start/protect/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Remove Image Background Task](actions/start-removebackgroundimage-task.md) | `GET https://api.iloveimg.com/v1/start/removebackgroundimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Repair PDF Task](actions/start-repair-task.md) | `GET /start/repair/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Repair Image Task](actions/start-repairimage-task.md) | `GET https://api.iloveimg.com/v1/start/repairimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Resize Image Task](actions/start-resizeimage-task.md) | `GET https://api.iloveimg.com/v1/start/resizeimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Rotate PDF Task](actions/start-rotate-task.md) | `GET /start/rotate/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Rotate Image Task](actions/start-rotateimage-task.md) | `GET https://api.iloveimg.com/v1/start/rotateimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Split PDF Task](actions/start-split-task.md) | `GET /start/split/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Unlock PDF Task](actions/start-unlock-task.md) | `GET /start/unlock/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Upscale Image Task](actions/start-upscaleimage-task.md) | `GET https://api.iloveimg.com/v1/start/upscaleimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Validate PDF/A Task](actions/start-validatepdfa-task.md) | `GET /start/validatepdfa/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Add PDF Watermark Task](actions/start-watermark-task.md) | `GET /start/watermark/:region` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Start Add Image Watermark Task](actions/start-watermarkimage-task.md) | `GET https://api.iloveimg.com/v1/start/watermarkimage` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Upload File From URL](actions/upload-file-from-url.md) | `POST https://:server/v1/upload` | [docs](https://www.iloveapi.com/docs/api-reference) |
| [Void Signature](actions/void-signature.md) | `POST /signature/void/:token_requester` | [docs](https://www.iloveapi.com/docs/api-reference) |
