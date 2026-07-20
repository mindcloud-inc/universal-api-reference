# <img src="https://images.mindcloud.co/apps/icons/cloud-fill_1776173128941.png" alt="CloudFill logo" width="28" height="28"> CloudFill: Universal API

Generate PDFs and inspect template metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudFill/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cloudfill.io
- **Vendor API docs:** https://www.cloudfill.io/help/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List PDFs](actions/list-pdfs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | POST | Generates a PDF from a CloudFill template. |
| [Get PDF Details](actions/get-pdf-details.md) | GET | Retrieves PDF metadata and field details from CloudFill. |
| [List PDFs](actions/list-pdfs.md) | GET | Retrieves available PDFs from your CloudFill account. |

