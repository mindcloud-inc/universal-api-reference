# <img src="https://images.mindcloud.co/apps/icons/digiparser_1774649626416.png" alt="DigiParser logo" width="28" height="28"> DigiParser: Universal API

Extract structured data from invoices, receipts, forms, and other documents with DigiParser OCR and parser workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digiParser/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digiparser.com
- **Vendor API docs:** https://www.digiparser.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Parsers](actions/list-parsers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/list-parsers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Documents](actions/delete-documents.md) | DELETE |  |
| [Get Document Data](actions/get-document-data.md) | GET |  |
| [Reprocess Document](actions/reprocess-document.md) | PUT |  |
| [Upload via URL](actions/upload-via-url.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Parsers](actions/list-parsers.md) | GET |  |

