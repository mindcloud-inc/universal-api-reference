# <img src="https://images.mindcloud.co/apps/icons/select-pdf_1776175791856.png" alt="SelectPdf logo" width="28" height="28"> SelectPdf: Universal API

SelectPdf provides cloud REST APIs to convert HTML to PDF, extract or search PDF text, merge PDFs, and inspect subscription usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/selectPdf/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://selectpdf.com/
- **Vendor API docs:** https://selectpdf.com/html-to-pdf-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Usage](actions/get-api-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST |  |
| [Convert URL to PDF](actions/convert-url-to-pdf.md) | POST |  |
| [Extract Text from PDF File](actions/extract-text-from-pdf-file.md) | GET |  |
| [Extract Text from PDF URL](actions/extract-text-from-pdfurl.md) | GET |  |
| [Get API Usage](actions/get-api-usage.md) | GET |  |
| [Merge PDFs from URLs](actions/merge-pd-fs-from-ur-ls.md) | POST |  |
| [Merge PDF Files](actions/merge-pdf-files.md) | POST |  |
| [Search PDF File](actions/search-pdf-file.md) | GET |  |
| [Search PDF URL](actions/search-pdfurl.md) | GET |  |

