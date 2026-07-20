# <img src="https://images.mindcloud.co/apps/icons/favicon-www-nutrient-io-48x48_1777546988279.png" alt="Nutrient - Watermark to PDF logo" width="28" height="28"> Nutrient - Watermark to PDF: Universal API

Add configurable text or image watermarks to PDF files using Nutrient DWS Processor API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientWatermarkToPDF/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io
- **Vendor API docs:** https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientWatermarkToPDF/latest/actions/add-image-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string",
  "logo": "string",
  "instructions": {
    "parts": [
      {
        "file": "document"
      }
    ],
    "actions": [
      {
        "type": "watermark",
        "image": "logo",
        "width": "50%"
      }
    ]
  }
}'
```

## Actions (5)

### Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md) | PUT | Updates a PDF with an image watermark in Nutrient. |
| [Add Last Page Watermark to PDF](actions/add-last-page-watermark-to-pdf.md) | PUT | Updates the last PDF page with a watermark in Nutrient. |
| [Add Multiple Watermarks to PDF](actions/add-multiple-watermarks-to-pdf.md) | PUT | Updates a PDF with multiple watermarks in Nutrient. |
| [Add Page Range Watermark to PDF](actions/add-page-range-watermark-to-pdf.md) | PUT | Updates selected PDF pages with a watermark in Nutrient. |
| [Add Text Watermark to PDF](actions/add-text-watermark-to-pdf.md) | PUT | Updates a PDF with a text watermark in Nutrient. |

