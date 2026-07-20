# iLovePDF: Native API Reference

A consolidated summary of iLovePDF's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.iloveapi.com/docs/api-reference
- **API base URL:** `https://api.ilovepdf.com/v1`

## Authentication

### API Keys

Use your iLovePDF Public Key and Secret Key from the same project.

### Credentials

- **API Key:** `apiKey` · required
- **Public Key:** `publicKey` · required · Project public key from the iLoveAPI API Keys page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.iloveapi.com/docs/api-reference#authentication)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compress PDF](actions/compress-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#compress-extra-parameters) |
| [Connect Task](actions/connect-task.md) | `POST https://:server/v1/task/next` | [docs](https://www.iloveapi.com/docs/api-reference#task) |
| [Create Signature Request](actions/create-signature-request.md) | `POST https://:server/v1/signature` | [docs](https://www.iloveapi.com/docs/api-reference#create-signature) |
| [Delete Task](actions/delete-task.md) | `DELETE https://:server/v1/task/:task` | [docs](https://www.iloveapi.com/docs/api-reference#task) |
| [Download Audit](actions/download-audit.md) | `GET https://:server/v1/signature/:tokenRequester/download-audit` | [docs](https://www.iloveapi.com/docs/api-reference#download-audit) |
| [Download Original Files](actions/download-original-files.md) | `GET https://:server/v1/signature/:tokenRequester/download-original` | [docs](https://www.iloveapi.com/docs/api-reference#download-original) |
| [Download Output Files](actions/download-output-files.md) | `GET https://:server/v1/download/:task` | [docs](https://www.iloveapi.com/docs/api-reference#download) |
| [Download Signed Files](actions/download-signed-files.md) | `GET https://:server/v1/signature/:tokenRequester/download-signed` | [docs](https://www.iloveapi.com/docs/api-reference#download-signed) |
| [Edit PDF](actions/edit-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#editpdf-extra-parameters) |
| [Extract PDF](actions/extract-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#extract-extra-parameters) |
| [Fix Receiver Email](actions/fix-receiver-email.md) | `PUT https://:server/v1/signature/signer/fix-email/:receiverTokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#fix-signer-email) |
| [Fix Signer Phone](actions/fix-signer-phone.md) | `PUT https://:server/v1/signature/signer/fix-phone/:signerTokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#fix-signer-phone) |
| [Get Receiver Info](actions/get-receiver-info.md) | `GET https://:server/v1/signature/receiver/info/:receiverTokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#get-signer) |
| [Get Server and Task ID](actions/get-server-and-task-id.md) | `GET /start/:tool/:region` | [docs](https://www.iloveapi.com/docs/api-reference#start) |
| [Get Signature Server and Task ID](actions/get-signature-server-and-task-id.md) | `GET /start/sign` | [docs](https://www.iloveapi.com/docs/api-reference#start) |
| [Get Signature Status](actions/get-signature-status.md) | `GET /signature/requesterview/:tokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#get-signature) |
| [HTML to PDF](actions/html-to-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#htmlpdf-extra-parameters) |
| [Increase Expiration Days](actions/increase-expiration-days.md) | `PUT https://:server/v1/signature/increase-expiration-days/:tokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#signature-increase-expiration-days) |
| [JPG to PDF](actions/jpg-to-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#imagepdf-extra-parameters) |
| [List Signatures](actions/list-signatures.md) | `GET https://:server/v1/signature/list` | [docs](https://www.iloveapi.com/docs/api-reference#list-signatures) |
| [List Tasks](actions/list-tasks.md) | `POST /task` | [docs](https://www.iloveapi.com/docs/api-reference#task) |
| [Merge PDF](actions/merge-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#merge-extra-parameters) |
| [Office to PDF](actions/office-to-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#officepdf-extra-parameters) |
| [Page Numbers](actions/page-numbers.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#pagenumber-extra-parameters) |
| [PDF OCR](actions/pdf-ocr.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#ocr-extra-parameters) |
| [PDF to JPG](actions/pdf-to-jpg.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#pdfjpg-extra-parameters) |
| [PDF to PDF/A](actions/pdf-to-pdfa.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#pdfa-extra-parameters) |
| [Process Files](actions/process-files.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#process) |
| [Protect PDF](actions/protect-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#protect-extra-parameters) |
| [Remove Uploaded File](actions/remove-uploaded-file.md) | `DELETE https://:server/v1/upload/:task/:serverFilename` | [docs](https://www.iloveapi.com/docs/api-reference#upload) |
| [Repair PDF](actions/repair-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#repair-extra-parameters) |
| [Rotate PDF](actions/rotate-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#rotate-extra-parameters) |
| [Send Reminders](actions/send-reminders.md) | `POST https://:server/v1/signature/sendReminder/:tokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#send-reminders) |
| [Split PDF](actions/split-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#split-extra-parameters) |
| [Unlock PDF](actions/unlock-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#unlock-extra-parameters) |
| [Upload File From URL](actions/upload-file-from-url.md) | `POST https://:server/v1/upload` | [docs](https://www.iloveapi.com/docs/api-reference#upload) |
| [Upload Local File](actions/upload-local-file.md) | `POST https://:server/v1/upload` | [docs](https://www.iloveapi.com/docs/api-reference#upload) |
| [Validate PDF/A](actions/validate-pdfa.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#validatepdfa-extra-parameters) |
| [Void Signature](actions/void-signature.md) | `PUT https://:server/v1/signature/void/:tokenRequester` | [docs](https://www.iloveapi.com/docs/api-reference#signature-void) |
| [Watermark PDF](actions/watermark-pdf.md) | `POST https://:server/v1/process` | [docs](https://www.iloveapi.com/docs/api-reference#watermark-extra-parameters) |
