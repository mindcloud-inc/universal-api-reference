# <img src="https://images.mindcloud.co/apps/icons/wise-ocr_1774978884090.png" alt="WiseOCR logo" width="28" height="28"> WiseOCR: Universal API

Extract receipt and invoice data into structured JSON

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wiseOCR/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wiseocr.com
- **Vendor API docs:** https://developers.wiseocr.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract Receipt Data From Text](actions/extract-receipt-data-from-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Extract Receipt Data From File](actions/extract-receipt-data-from-file.md) | GET | Retrieves extracted receipt data from WiseOCR using an uploaded file. |
| [Extract Receipt Data From Text](actions/extract-receipt-data-from-text.md) | GET | Retrieves extracted receipt data from WiseOCR using text. |
| [Extract Receipt Data From URL](actions/extract-receipt-data-from-url.md) | GET | Retrieves extracted receipt data from WiseOCR using a file URL. |

