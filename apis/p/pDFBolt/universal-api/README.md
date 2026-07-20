# <img src="https://images.mindcloud.co/apps/icons/pdf-bolt_1775744962701.png" alt="PDFBolt logo" width="28" height="28"> PDFBolt: Universal API

Generate PDFs from URLs, HTML, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFBolt/latest
- **Category:** Content & Files / Storage
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdfbolt.com
- **Vendor API docs:** https://pdfbolt.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF from HTML](actions/create-pdf-from-html.md) | POST | Creates a PDF from HTML in PDFBolt. |
| [Create PDF from Template](actions/create-pdf-from-template.md) | POST | Creates a PDF from a template in PDFBolt. |
| [Create PDF from URL](actions/create-pdf-from-url.md) | POST | Creates a PDF from a URL in PDFBolt. |

### Pdf Link

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF Link from HTML](actions/create-pdf-link-from-html.md) | POST | Creates a PDF download link from HTML in PDFBolt. |
| [Create PDF Link from Template](actions/create-pdf-link-from-template.md) | POST | Creates a PDF download link from a template in PDFBolt. |
| [Create PDF Link from URL](actions/create-pdf-link-from-url.md) | POST | Creates a PDF download link from a URL in PDFBolt. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage details from PDFBolt. |

