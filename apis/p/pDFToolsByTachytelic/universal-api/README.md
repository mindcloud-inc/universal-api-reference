# <img src="https://images.mindcloud.co/apps/icons/favicon-learn-microsoft-com-48x48_1777641410814.png" alt="PDF Tools by Tachytelic logo" width="28" height="28"> PDF Tools by Tachytelic: Universal API

Free PDF utility actions for merging, splitting, extracting pages and text, optimizing file size, and managing PDF metadata through Tachytelic's public PDF Tools API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFToolsByTachytelic/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tachytelic.net/pdf-tools-for-power-automate/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract PDF Pages](actions/extract-pdf-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/extract-pdf-pages?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content&pageRange=1-3%2C7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Pages](actions/extract-pdf-pages.md) | GET |  |
| [Extract Text from PDF](actions/extract-text-from-pdf.md) | GET |  |
| [Get PDF Info](actions/get-pdf-info.md) | GET |  |
| [Merge PDFs](actions/merge-pdfs.md) | GET |  |
| [Optimize PDF](actions/optimize-pdf.md) | GET |  |
| [Set PDF Metadata](actions/set-pdf-metadata.md) | GET |  |
| [Split PDF](actions/split-pdf.md) | GET |  |

