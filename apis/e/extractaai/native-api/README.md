# Extracta.ai: Native API Reference

A consolidated summary of Extracta.ai's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.extracta.ai/extracta.ai
- **API base URL:** `https://api.extracta.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.extracta.ai/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Classification](actions/create-classification.md) | `POST /documentClassification/createClassification` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/1.-create-classification) |
| [Create Extraction](actions/create-extraction.md) | `POST /createExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/1.-create-extraction) |
| [Delete Classification](actions/delete-classification.md) | `DELETE /documentClassification/deleteClassification` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/4.-delete-data/4.1-delete-classification) |
| [Delete Classification Batch](actions/delete-classification-batch.md) | `DELETE /documentClassification/deleteBatch` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/4.-delete-data/4.2-delete-batch) |
| [Delete Classification Files](actions/delete-classification-files.md) | `DELETE /documentClassification/deleteFiles` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/4.-delete-data/4.3-delete-files) |
| [Delete Extraction](actions/delete-extraction.md) | `DELETE /deleteExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/4.-delete-extraction) |
| [Delete Extraction Batch](actions/delete-extraction-batch.md) | `DELETE /deleteExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/4.-delete-extraction) |
| [Delete Extraction File](actions/delete-extraction-file.md) | `DELETE /deleteExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/4.-delete-extraction) |
| [Get Classification Batch Results](actions/get-classification-batch-results.md) | `POST /documentClassification/getResults` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/6.-get-results) |
| [Get Classification File Results](actions/get-classification-file-results.md) | `POST /documentClassification/getResults` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/6.-get-results) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/7.-get-credits) |
| [Get Extraction Batch Results](actions/get-extraction-batch-results.md) | `POST /getBatchResults` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/6.-get-results) |
| [Get Extraction File Results](actions/get-extraction-file-results.md) | `POST /getBatchResults` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/6.-get-results) |
| [Update Classification](actions/update-classification.md) | `PATCH /documentClassification/updateClassification` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/3.-update-classification) |
| [Update Extraction](actions/update-extraction.md) | `PATCH /updateExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/3.-update-extraction) |
| [Upload Files to Classification](actions/upload-files-to-classification.md) | `POST /documentClassification/uploadFiles` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/5.-upload-files) |
| [Upload Files to Classification Batch](actions/upload-files-to-classification-batch.md) | `POST /documentClassification/uploadFiles` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/5.-upload-files) |
| [Upload Files to Extraction](actions/upload-files-to-extraction.md) | `POST /uploadFiles` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/5.-upload-files) |
| [Upload Files to Extraction Batch](actions/upload-files-to-extraction-batch.md) | `POST /uploadFiles` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/5.-upload-files) |
| [View Classification](actions/view-classification.md) | `POST /documentClassification/viewClassification` | [docs](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/2.-view-classification) |
| [View Extraction](actions/view-extraction.md) | `POST /viewExtraction` | [docs](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/2.-view-extraction) |
