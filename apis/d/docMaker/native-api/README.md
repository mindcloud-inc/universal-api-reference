# DocMaker: Native API Reference

A consolidated summary of DocMaker's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://docmaker.co/api
- **OpenAPI specification:** https://docmaker.co/docMaker-swagger.json
- **API base URL:** `https://api.v2.docmaker.co`

## Authentication

### API Key

Authenticate DocMaker API requests with an account API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docmaker.co/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create DOCX from DOCX Template URL](actions/create-docx-from-docx-template-url.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL And Upload Output File](actions/create-docx-or-pdf-from-docx-template-url-and-upload-output-file.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL As Base64 Response](actions/create-docx-or-pdf-from-docx-template-url-as-base64-response.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL With Metadata](actions/create-docx-or-pdf-from-docx-template-url-with-metadata.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL With Webhook](actions/create-docx-or-pdf-from-docx-template-url-with-webhook.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL With Webhook JSON](actions/create-docx-or-pdf-from-docx-template-url-with-webhook-json.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create DOCX Or PDF from DOCX Template URL With Webhook Token](actions/create-docx-or-pdf-from-docx-template-url-with-webhook-token.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create Landscape Webpage PDF](actions/create-landscape-webpage-pdf.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create PDF from DOCX Template URL](actions/create-pdf-from-docx-template-url.md) | `POST /docx_fill_convert` | [docs](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters) |
| [Create PDF from Webpage](actions/create-pdf-from-webpage.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF And Upload Output File](actions/create-webpage-pdf-and-upload-output-file.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF As Base64 Response](actions/create-webpage-pdf-as-base64-response.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Custom Viewport](actions/create-webpage-pdf-with-custom-viewport.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Delayed Load Time](actions/create-webpage-pdf-with-delayed-load-time.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Footer](actions/create-webpage-pdf-with-footer.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Footer HTML](actions/create-webpage-pdf-with-footer-html.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Locale And Timezone Overrides](actions/create-webpage-pdf-with-locale-and-timezone-overrides.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Metadata](actions/create-webpage-pdf-with-metadata.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Page Ranges](actions/create-webpage-pdf-with-page-ranges.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Webhook](actions/create-webpage-pdf-with-webhook.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Create Webpage PDF With Webhook Object ID and Type](actions/create-webpage-pdf-with-webhook-object-id-and-type.md) | `POST /page_pdf` | [docs](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters) |
| [Fill PDF Form From Template ID](actions/fill-pdf-form-from-template-id.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template ID And Upload Output File](actions/fill-pdf-form-from-template-id-and-upload-output-file.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template ID As Base64 Response](actions/fill-pdf-form-from-template-id-as-base64-response.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template ID With Custom Font Size](actions/fill-pdf-form-from-template-id-with-custom-font-size.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template ID With Metadata](actions/fill-pdf-form-from-template-id-with-metadata.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template ID With Webhook](actions/fill-pdf-form-from-template-id-with-webhook.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template URL](actions/fill-pdf-form-from-template-url.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template URL And Upload Output File](actions/fill-pdf-form-from-template-url-and-upload-output-file.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template URL As Base64 Response](actions/fill-pdf-form-from-template-url-as-base64-response.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template URL With Custom Font Size](actions/fill-pdf-form-from-template-url-with-custom-font-size.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Fill PDF Form From Template URL With Webhook](actions/fill-pdf-form-from-template-url-with-webhook.md) | `POST /fill_pdf` | [docs](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters) |
| [Get Job Result File Details](actions/get-job-result-file-details.md) | `GET /jobs/:jobId` | [docs](https://docmaker.co/docMaker-swagger.json) |
| [Get Job Status](actions/get-job-status.md) | `GET /jobs/:jobId` | [docs](https://docmaker.co/docMaker-swagger.json) |
| [Get Remaining Credits From Job Status](actions/get-remaining-credits-from-job-status.md) | `GET /jobs/:jobId` | [docs](https://docmaker.co/docMaker-swagger.json) |
