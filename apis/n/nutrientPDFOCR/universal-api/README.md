# <img src="https://images.mindcloud.co/apps/icons/favicon-www-nutrient-io-48x48_1777546917656.png" alt="Nutrient - PDF OCR logo" width="28" height="28"> Nutrient - PDF OCR: Universal API

Extract text from scanned PDFs and images by creating searchable PDF outputs with Nutrient DWS Processor OCR.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientPDFOCR/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io
- **Vendor API docs:** https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [OCR Document](actions/ocr-document.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document?connectionId=$CONNECTION_ID&file=Upload%20a%20scanned%20PDF%20or%20image%20file&data.language=english" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [OCR Document](actions/ocr-document.md) | GET | Retrieves a searchable PDF from Nutrient using OCR. |

