# <img src="https://images.mindcloud.co/apps/icons/encodian_1777477336490.jpeg" alt="Encodian - Convert logo" width="28" height="28"> Encodian - Convert: Universal API

Encodian Flowr Convert provides file and data conversion actions for documents, PDFs, images, HTML, JSON, email, CAD, and Microsoft Office formats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianConvert/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr/
- **Vendor API docs:** https://support.encodian.com/hc/en-gb/articles/22002408782108-Encodian-Convert-Connector

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get an Operation Status](actions/conversion-get-operation-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/conversion-get-operation-status?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get an Operation Status](actions/conversion-get-operation-status.md) | GET | Retrieves an operation status from Encodian - Convert. |
| [Convert - CAD](actions/convert-cad.md) | POST | Creates a converted file from a CAD file in Encodian - Convert. |
| [Convert - Email](actions/convert-email.md) | POST | Creates a PDF file from an email and attachments in Encodian - Convert. |
| [Convert - Excel](actions/convert-excel.md) | POST | Creates a converted file from an Excel document in Encodian - Convert. |
| [Convert - File to PDF](actions/convert-file-to-pdf.md) | POST | Creates a PDF file from another file in Encodian - Convert. |
| [Convert - HEIC to PDF](actions/convert-heic-to-pdf.md) | POST | Creates a PDF file from a HEIC image in Encodian - Convert. |
| [Convert - HTML to Image](actions/convert-html-to-image.md) | POST | Creates an image file from HTML or a web URL in Encodian - Convert. |
| [Convert - HTML to PDF](actions/convert-html-to-pdf.md) | POST | Creates a PDF file from HTML or a web URL in Encodian - Convert. |
| [Convert - HTML to PDF (V2)](actions/convert-html-to-pdf-v2.md) | POST | Creates a PDF file from HTML or a web URL in Encodian - Convert. |
| [Convert - HTML to Word](actions/convert-html-to-word.md) | POST | Creates a Word file from HTML or a web URL in Encodian - Convert. |
| [Convert - Image to PDF](actions/convert-image-to-pdf.md) | POST | Creates a PDF file from an image in Encodian - Convert. |
| [Convert - JSON to Excel](actions/convert-json-to-excel.md) | POST | Creates an Excel file from JSON in Encodian - Convert. |
| [Convert - PDF to Excel](actions/convert-pdf-to-excel.md) | POST | Creates an Excel file from a PDF in Encodian - Convert. |
| [Convert - PDF to Images](actions/convert-pdf-to-images.md) | POST | Creates image files from a PDF in Encodian - Convert. |
| [Convert - PDF to JPG](actions/convert-pdf-to-jpg.md) | POST | Creates a JPG file from a PDF in Encodian - Convert. |
| [Convert - PDF to PDFA](actions/convert-pdf-to-pdfa.md) | POST | Creates a PDF/A file from a PDF in Encodian - Convert. |
| [Convert - PDF to PNG](actions/convert-pdf-to-png.md) | POST | Creates a PNG file from a PDF in Encodian - Convert. |
| [Convert - PDF to TIFF](actions/convert-pdf-to-tiff.md) | POST | Creates a TIFF file from a PDF in Encodian - Convert. |
| [Convert - PDF to Word](actions/convert-pdf-to-word.md) | POST | Creates a Word file from a PDF in Encodian - Convert. |
| [Convert - PowerPoint](actions/convert-power-point.md) | POST | Creates a converted file from a PowerPoint document in Encodian - Convert. |
| [Convert - Text to PDF](actions/convert-text-to-pdf.md) | POST | Creates a PDF file from text in Encodian - Convert. |
| [Convert - Visio](actions/convert-visio.md) | POST | Creates a converted file from a Visio document in Encodian - Convert. |
| [Convert - Word](actions/convert-word.md) | POST | Creates a converted file from a Word document in Encodian - Convert. |
| [Convert - Word to PDF Form](actions/convert-word-to-pdf-form.md) | POST | Creates a PDF form from a Word document in Encodian - Convert. |

