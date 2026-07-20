# <img src="https://images.mindcloud.co/apps/icons/id-tc0e-mlm-b-logos_1776102926955.jpeg" alt="Extracta.ai logo" width="28" height="28"> Extracta.ai: Universal API

Extract document data and classify files with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/extractaai/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://extracta.ai
- **Vendor API docs:** https://docs.extracta.ai/extracta.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Classification

| Action | Method | Description |
| --- | --- | --- |
| [Create Classification](actions/create-classification.md) | POST | Creates a new classification in Extracta.ai. |
| [Delete Classification](actions/delete-classification.md) | DELETE | Deletes an existing classification from Extracta.ai. |
| [Update Classification](actions/update-classification.md) | PUT | Updates an existing classification in Extracta.ai. |
| [View Classification](actions/view-classification.md) | GET | Retrieves a classification from Extracta.ai. |

### Classification Batch

| Action | Method | Description |
| --- | --- | --- |
| [Delete Classification Batch](actions/delete-classification-batch.md) | DELETE | Deletes a classification batch from Extracta.ai. |
| [Upload Files to Classification Batch](actions/upload-files-to-classification-batch.md) | POST | Uploads files to a classification batch in Extracta.ai. |

### Classification File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Classification Files](actions/delete-classification-files.md) | DELETE | Deletes classification files from Extracta.ai. |
| [Upload Files to Classification](actions/upload-files-to-classification.md) | POST | Uploads files to a classification in Extracta.ai. |

### Classification Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Classification Batch Results](actions/get-classification-batch-results.md) | GET | Retrieves classification batch results from Extracta.ai. |
| [Get Classification File Results](actions/get-classification-file-results.md) | GET | Retrieves classification file results from Extracta.ai. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves credits from Extracta.ai. |

### Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Create Extraction](actions/create-extraction.md) | POST | Creates a new extraction in Extracta.ai. |
| [Delete Extraction](actions/delete-extraction.md) | DELETE | Deletes an existing extraction from Extracta.ai. |
| [Update Extraction](actions/update-extraction.md) | PUT | Updates an existing extraction in Extracta.ai. |
| [View Extraction](actions/view-extraction.md) | GET | Retrieves an extraction from Extracta.ai. |

### Extraction Batch

| Action | Method | Description |
| --- | --- | --- |
| [Delete Extraction Batch](actions/delete-extraction-batch.md) | DELETE | Deletes an extraction batch from Extracta.ai. |
| [Upload Files to Extraction Batch](actions/upload-files-to-extraction-batch.md) | POST | Uploads files to an extraction batch in Extracta.ai. |

### Extraction File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Extraction File](actions/delete-extraction-file.md) | DELETE | Deletes an extraction file from Extracta.ai. |
| [Upload Files to Extraction](actions/upload-files-to-extraction.md) | POST | Uploads files to an extraction in Extracta.ai. |

### Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Extraction Batch Results](actions/get-extraction-batch-results.md) | GET | Retrieves extraction batch results from Extracta.ai. |
| [Get Extraction File Results](actions/get-extraction-file-results.md) | GET | Retrieves extraction file results from Extracta.ai. |

