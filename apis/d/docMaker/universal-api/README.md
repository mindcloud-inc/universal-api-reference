# <img src="https://images.mindcloud.co/apps/icons/doc-maker_1773954159779.png" alt="DocMaker logo" width="28" height="28"> DocMaker: Universal API

Create, fill, and render PDFs from templates and webpages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docMaker/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docmaker.co
- **Vendor API docs:** https://docmaker.co/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Job Result File Details](actions/get-job-result-file-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-result-file-details?connectionId=$CONNECTION_ID&jobId=7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create DOCX Or PDF from DOCX Template URL And Upload Output File](actions/create-docx-or-pdf-from-docx-template-url-and-upload-output-file.md) | POST | Creates a DOCX or PDF from a template URL and uploads output in DocMaker. |
| [Create DOCX Or PDF from DOCX Template URL As Base64 Response](actions/create-docx-or-pdf-from-docx-template-url-as-base64-response.md) | POST | Creates a DOCX or PDF from a template URL as Base64 in DocMaker. |
| [Create DOCX Or PDF from DOCX Template URL With Metadata](actions/create-docx-or-pdf-from-docx-template-url-with-metadata.md) | POST | Creates a DOCX or PDF from a template URL with metadata in DocMaker. |
| [Create DOCX Or PDF from DOCX Template URL With Webhook](actions/create-docx-or-pdf-from-docx-template-url-with-webhook.md) | POST | Creates a DOCX or PDF from a template URL with webhook in DocMaker. |
| [Create DOCX Or PDF from DOCX Template URL With Webhook JSON](actions/create-docx-or-pdf-from-docx-template-url-with-webhook-json.md) | POST | Creates a DOCX or PDF from a template URL with webhook JSON in DocMaker. |
| [Create DOCX Or PDF from DOCX Template URL With Webhook Token](actions/create-docx-or-pdf-from-docx-template-url-with-webhook-token.md) | POST | Creates a DOCX or PDF from a template URL with webhook auth in DocMaker. |

### Docx

| Action | Method | Description |
| --- | --- | --- |
| [Create DOCX from DOCX Template URL](actions/create-docx-from-docx-template-url.md) | POST | Creates a DOCX from a DOCX template URL in DocMaker. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Result File Details](actions/get-job-result-file-details.md) | GET | Retrieves result file details from a DocMaker job. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves job status from DocMaker. |
| [Get Remaining Credits From Job Status](actions/get-remaining-credits-from-job-status.md) | GET | Retrieves remaining credits from a DocMaker job. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create Landscape Webpage PDF](actions/create-landscape-webpage-pdf.md) | POST | Creates a landscape webpage PDF in DocMaker. |
| [Create PDF from DOCX Template URL](actions/create-pdf-from-docx-template-url.md) | POST | Creates a PDF from a DOCX template URL in DocMaker. |
| [Create PDF from Webpage](actions/create-pdf-from-webpage.md) | POST | Creates a PDF from a webpage in DocMaker. |
| [Create Webpage PDF And Upload Output File](actions/create-webpage-pdf-and-upload-output-file.md) | POST | Creates a webpage PDF and uploads output in DocMaker. |
| [Create Webpage PDF As Base64 Response](actions/create-webpage-pdf-as-base64-response.md) | POST | Creates a webpage PDF as Base64 in DocMaker. |
| [Create Webpage PDF With Custom Viewport](actions/create-webpage-pdf-with-custom-viewport.md) | POST | Creates a webpage PDF with custom viewport in DocMaker. |
| [Create Webpage PDF With Delayed Load Time](actions/create-webpage-pdf-with-delayed-load-time.md) | POST | Creates a webpage PDF with delayed load time in DocMaker. |
| [Create Webpage PDF With Footer](actions/create-webpage-pdf-with-footer.md) | POST | Creates a webpage PDF with a footer in DocMaker. |
| [Create Webpage PDF With Footer HTML](actions/create-webpage-pdf-with-footer-html.md) | POST | Creates a webpage PDF with HTML footer in DocMaker. |
| [Create Webpage PDF With Locale And Timezone Overrides](actions/create-webpage-pdf-with-locale-and-timezone-overrides.md) | POST | Creates a webpage PDF with locale and timezone overrides in DocMaker. |
| [Create Webpage PDF With Metadata](actions/create-webpage-pdf-with-metadata.md) | POST | Creates a webpage PDF with metadata in DocMaker. |
| [Create Webpage PDF With Page Ranges](actions/create-webpage-pdf-with-page-ranges.md) | POST | Creates a webpage PDF with page ranges in DocMaker. |
| [Create Webpage PDF With Webhook](actions/create-webpage-pdf-with-webhook.md) | POST | Creates a webpage PDF with webhook in DocMaker. |
| [Create Webpage PDF With Webhook Object ID and Type](actions/create-webpage-pdf-with-webhook-object-id-and-type.md) | POST | Creates a webpage PDF with webhook object details in DocMaker. |
| [Fill PDF Form From Template ID](actions/fill-pdf-form-from-template-id.md) | POST | Creates a filled PDF form from a template ID in DocMaker. |
| [Fill PDF Form From Template ID And Upload Output File](actions/fill-pdf-form-from-template-id-and-upload-output-file.md) | POST | Creates a filled PDF form from a template ID and uploads output in DocMaker. |
| [Fill PDF Form From Template ID As Base64 Response](actions/fill-pdf-form-from-template-id-as-base64-response.md) | POST | Creates a filled PDF form from a template ID as Base64 in DocMaker. |
| [Fill PDF Form From Template ID With Custom Font Size](actions/fill-pdf-form-from-template-id-with-custom-font-size.md) | POST | Creates a PDF form from a template ID with custom font size in DocMaker. |
| [Fill PDF Form From Template ID With Metadata](actions/fill-pdf-form-from-template-id-with-metadata.md) | POST | Creates a filled PDF form from a template ID with metadata in DocMaker. |
| [Fill PDF Form From Template ID With Webhook](actions/fill-pdf-form-from-template-id-with-webhook.md) | POST | Creates a filled PDF form from a template ID with webhook in DocMaker. |
| [Fill PDF Form From Template URL](actions/fill-pdf-form-from-template-url.md) | POST | Creates a filled PDF form from a template URL in DocMaker. |
| [Fill PDF Form From Template URL And Upload Output File](actions/fill-pdf-form-from-template-url-and-upload-output-file.md) | POST | Creates a filled PDF form from a template URL and uploads output in DocMaker. |
| [Fill PDF Form From Template URL As Base64 Response](actions/fill-pdf-form-from-template-url-as-base64-response.md) | POST | Creates a filled PDF form from a template URL as Base64 in DocMaker. |
| [Fill PDF Form From Template URL With Custom Font Size](actions/fill-pdf-form-from-template-url-with-custom-font-size.md) | POST | Creates a PDF form from a template URL with custom font size in DocMaker. |
| [Fill PDF Form From Template URL With Webhook](actions/fill-pdf-form-from-template-url-with-webhook.md) | POST | Creates a filled PDF form from a template URL with webhook in DocMaker. |

