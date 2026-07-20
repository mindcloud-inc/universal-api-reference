# <img src="https://images.mindcloud.co/apps/icons/google-cloud-document-ai_1776347645648.png" alt="Google Cloud Document AI logo" width="28" height="28"> Google Cloud Document AI: Universal API

Use Google Cloud Document AI to extract, classify, train, evaluate, and manage document processors through the stable v1 REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleCloudDocumentAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloud.google.com/document-ai
- **Vendor API docs:** https://cloud.google.com/document-ai/docs/reference/rest/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Processor Types](actions/list-processor-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/list-processor-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Batch Process Documents With Processor](actions/batch-process-documents-with-processor.md) | GET | Batch processes documents with a Google Cloud Document AI processor. |
| [Batch Process Documents With Processor Version](actions/batch-process-documents-with-processor-version.md) | GET | Batch processes documents with a Google Cloud Document AI processor version. |
| [Cancel Location Operation](actions/cancel-location-operation.md) | PUT | Cancels an operation in a Google Cloud Document AI location. |
| [Create Processor](actions/create-processor.md) | POST | Creates a new processor in Google Cloud Document AI. |
| [Create Schema](actions/create-schema.md) | POST | Creates a new schema in Google Cloud Document AI. |
| [Create Schema Version](actions/create-schema-version.md) | POST | Creates a new schema version in Google Cloud Document AI. |
| [Delete Processor](actions/delete-processor.md) | DELETE | Deletes a processor from Google Cloud Document AI. |
| [Delete Processor Version](actions/delete-processor-version.md) | DELETE | Deletes a processor version from Google Cloud Document AI. |
| [Delete Schema](actions/delete-schema.md) | DELETE | Deletes a schema from Google Cloud Document AI. |
| [Delete Schema Version](actions/delete-schema-version.md) | DELETE | Deletes a schema version from Google Cloud Document AI. |
| [Deploy Processor Version](actions/deploy-processor-version.md) | PUT | Deploys a processor version in Google Cloud Document AI. |
| [Disable Processor](actions/disable-processor.md) | PUT | Disables a processor in Google Cloud Document AI. |
| [Enable Processor](actions/enable-processor.md) | PUT | Enables a processor in Google Cloud Document AI. |
| [Evaluate Processor Version](actions/evaluate-processor-version.md) | GET | Evaluates a processor version in Google Cloud Document AI. |
| [Fetch Processor Types](actions/fetch-processor-types.md) | GET | Fetches processor types from Google Cloud Document AI. |
| [Generate Schema Version](actions/generate-schema-version.md) | POST | Generates a schema version in Google Cloud Document AI. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Google Cloud Document AI. |
| [Get Location Operation](actions/get-location-operation.md) | GET | Retrieves an operation from a Google Cloud Document AI location. |
| [Get Processor](actions/get-processor.md) | GET | Retrieves a processor from Google Cloud Document AI. |
| [Get Processor Type](actions/get-processor-type.md) | GET | Retrieves a processor type from Google Cloud Document AI. |
| [Get Processor Version](actions/get-processor-version.md) | GET | Retrieves a processor version from Google Cloud Document AI. |
| [Get Processor Version Evaluation](actions/get-processor-version-evaluation.md) | GET | Retrieves a processor version evaluation from Google Cloud Document AI. |
| [Get Schema](actions/get-schema.md) | GET | Retrieves a schema from Google Cloud Document AI. |
| [Get Schema Version](actions/get-schema-version.md) | GET | Retrieves a schema version from Google Cloud Document AI. |
| [List Location Operations](actions/list-location-operations.md) | GET | Finds operations in a Google Cloud Document AI location. |
| [List Locations](actions/list-locations.md) | GET | Finds locations in Google Cloud Document AI. |
| [List Processor Types](actions/list-processor-types.md) | GET | Finds processor types in Google Cloud Document AI. |
| [List Processor Version Evaluations](actions/list-processor-version-evaluations.md) | GET | Finds processor version evaluations in Google Cloud Document AI. |
| [List Processor Versions](actions/list-processor-versions.md) | GET | Finds processor versions in Google Cloud Document AI. |
| [List Processors](actions/list-processors.md) | GET | Finds processors in a Google Cloud Document AI location. |
| [List Schema Versions](actions/list-schema-versions.md) | GET | Finds schema versions in Google Cloud Document AI. |
| [List Schemas](actions/list-schemas.md) | GET | Finds schemas in Google Cloud Document AI. |
| [Process Document With Processor](actions/process-document-with-processor.md) | GET | Processes a document with a Google Cloud Document AI processor. |
| [Process Document With Processor Version](actions/process-document-with-processor-version.md) | GET | Processes a document with a Google Cloud Document AI processor version. |
| [Review Document With Human Review Config](actions/review-document-with-human-review-config.md) | POST | Creates a human review request in Google Cloud Document AI. |
| [Set Default Processor Version](actions/set-default-processor-version.md) | PUT | Sets the default processor version in Google Cloud Document AI. |
| [Train Processor Version](actions/train-processor-version.md) | POST | Trains a processor version in Google Cloud Document AI. |
| [Undeploy Processor Version](actions/undeploy-processor-version.md) | PUT | Undeploys a processor version in Google Cloud Document AI. |
| [Update Schema](actions/update-schema.md) | PUT | Updates an existing schema in Google Cloud Document AI. |
| [Update Schema Version](actions/update-schema-version.md) | PUT | Updates an existing schema version in Google Cloud Document AI. |

