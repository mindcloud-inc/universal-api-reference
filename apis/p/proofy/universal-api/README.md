# <img src="https://images.mindcloud.co/apps/icons/proofy_1776187692979.png" alt="Proofy logo" width="28" height="28"> Proofy: Universal API

Verify emails in real time and process batch or file checks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proofy/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://proofy.io/
- **Vendor API docs:** https://docs.proofy.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Batch Status](actions/check-batch-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Batch Request

| Action | Method | Description |
| --- | --- | --- |
| [Check Batch Status](actions/check-batch-status.md) | GET |  |
| [Create Batch Request](actions/create-batch-request.md) | POST |  |
| [Delete Batch Request](actions/delete-batch-request.md) | DELETE |  |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Results](actions/get-batch-results.md) | GET |  |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Credits](actions/get-available-credits.md) | GET |  |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Single Email](actions/verify-single-email.md) | GET |  |

### File Request

| Action | Method | Description |
| --- | --- | --- |
| [Check File Status](actions/check-file-status.md) | GET |  |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Upload File](actions/upload-file.md) | POST |  |
| [Upload File by URL](actions/upload-file-by-url.md) | POST |  |

### File Result

| Action | Method | Description |
| --- | --- | --- |
| [Download File Results](actions/download-file-results.md) | GET |  |

