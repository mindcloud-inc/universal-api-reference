# <img src="https://images.mindcloud.co/apps/icons/favicon-www-nutrient-io-48x48_1777547080136.png" alt="Nutrient Document Converter logo" width="28" height="28"> Nutrient Document Converter: Universal API

Convert, generate, OCR, watermark, secure, archive, and render documents with Nutrient DWS Processor APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientDocumentConverter/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io/
- **Vendor API docs:** https://www.nutrient.io/guides/dws-processor/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf?connectionId=$CONNECTION_ID&markdown=%23%20Hello%20from%20Nutrient%5Cn%5CnThis%20PDF%20was%20generated%20from%20Markdown." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | GET | Converts Markdown to PDF in Nutrient. |
| [Convert Remote Document to Image](actions/convert-remote-document-to-image.md) | GET | Converts a remote document to images in Nutrient. |
| [Convert Remote Document to PDF](actions/convert-remote-document-to-pdf.md) | GET | Converts a remote document to PDF in Nutrient. |
| [Convert Remote Image to PDF](actions/convert-remote-image-to-pdf.md) | GET | Converts a remote image to PDF in Nutrient. |
| [Convert Remote PDF to Image](actions/convert-remote-pdf-to-image.md) | GET | Converts a remote PDF to images in Nutrient. |
| [Convert Remote PDF to PDF/A](actions/convert-remote-pdf-to-pdfa.md) | GET | Converts a remote PDF to PDF/A in Nutrient. |
| [Flatten Remote PDF](actions/flatten-remote-pdf.md) | GET | Flattens a remote PDF in Nutrient. |
| [Generate PDF from Remote HTML](actions/generate-pdf-from-remote-html.md) | GET | Generates a PDF from remote HTML in Nutrient. |
| [OCR Remote Document](actions/ocr-remote-document.md) | GET | Applies OCR to a remote document in Nutrient. |
| [Protect Remote PDF](actions/protect-remote-pdf.md) | GET | Protects a remote PDF in Nutrient. |
| [Run Build Instructions](actions/run-build-instructions.md) | GET | Builds a document from custom instructions in Nutrient. |
| [Watermark Remote PDF](actions/watermark-remote-pdf.md) | GET | Adds a watermark to a remote PDF in Nutrient. |

