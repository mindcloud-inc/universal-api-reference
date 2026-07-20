# <img src="https://images.mindcloud.co/apps/icons/nutrient-document-web-services-api_1774905184989.png" alt="Nutrient Document Web Services logo" width="28" height="28"> Nutrient Document Web Services: Universal API

Cloud-based document processing APIs for PDF generation, conversion, OCR, redaction, signing, and extraction.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientDocumentWebServicesAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io/api/
- **Vendor API docs:** https://www.nutrient.io/api/reference/public/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze Build Request](actions/analyze-build-request.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/analyze-build-request?connectionId=$CONNECTION_ID&parts%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information from Nutrient Document Web Services API. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | PUT | Updates a document with watermarks in Nutrient Document Web Services API. |
| [AI Redact Sensitive Information](actions/ai-redact-sensitive-information.md) | PUT | Updates a document by redacting sensitive information in Nutrient Document Web Services API. |
| [Analyze Build Request](actions/analyze-build-request.md) | GET | Analyzes a document build request in Nutrient Document Web Services API. |
| [Build Document](actions/build-document.md) | POST | Creates a processed document in Nutrient Document Web Services API. |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST | Creates a PDF document from HTML in Nutrient Document Web Services API. |
| [Convert to PDF](actions/convert-to-pdf.md) | POST | Creates a PDF document in Nutrient Document Web Services API. |
| [Digitally Sign PDF](actions/digitally-sign-pdf.md) | PUT | Updates a PDF document with a digital signature in Nutrient Document Web Services API. |
| [PDF/UA Auto-Tagging](actions/pdf-ua-auto-tagging.md) | POST | Creates a PDF/UA document in Nutrient Document Web Services API. |
| [Perform OCR](actions/perform-ocr.md) | POST | Creates a searchable document with OCR in Nutrient Document Web Services API. |
| [Redact Documents](actions/redact-documents.md) | PUT | Updates a document with redactions in Nutrient Document Web Services API. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate API Token](actions/generate-api-token.md) | POST | Creates an API token in Nutrient Document Web Services API. |
| [Revoke API Token](actions/revoke-api-token.md) | DELETE | Deletes an API token from Nutrient Document Web Services API. |

