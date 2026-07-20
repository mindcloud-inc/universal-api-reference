# <img src="https://images.mindcloud.co/apps/icons/receipt-bot_1776872137861.png" alt="Receipt Bot logo" width="28" height="28"> Receipt Bot: Universal API

Upload documents, extract data, and automate bookkeeping workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/receiptBot/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.receipt-bot.com
- **Vendor API docs:** https://documenter.getpostman.com/view/14388213/2sA3kYjLPj

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Statement Details](actions/get-statement-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/get-statement-details?connectionId=$CONNECTION_ID&documentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a base64-encoded file to Receipt Bot. |

### Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Details](actions/get-statement-details.md) | GET | Retrieves statement details from Receipt Bot by document ID. |

