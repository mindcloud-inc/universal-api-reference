# <img src="https://images.mindcloud.co/apps/icons/pdfai_1774989625434.png" alt="PDF API Hub logo" width="28" height="28"> PDF API Hub: Universal API

Fill PDFs, add images, and apply watermarks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFAPIHub/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prefillpdf.com
- **Vendor API docs:** https://api.prefillpdf.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract Text From URL](actions/extract-text-from-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url?connectionId=$CONNECTION_ID&fileUrl=https%3A%2F%2Fwww.adobe.com%2Fsupport%2Fproducts%2Fenterprise%2Fknowledgecenter%2Fmedia%2Fc4611_sample_explain.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Extract CSV From File](actions/extract-csv-from-file.md) | GET |  |
| [Extract Text From File](actions/extract-text-from-file.md) | GET |  |
| [Extract Text From URL](actions/extract-text-from-url.md) | GET |  |
| [Fill PDF](actions/fill-pdf.md) | POST |  |
| [Watermark PDF](actions/watermark-pdf.md) | POST |  |

