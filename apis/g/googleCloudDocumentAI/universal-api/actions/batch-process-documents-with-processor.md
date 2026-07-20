# Google Cloud Document AI: Batch Process Documents With Processor

Batch processes documents with a Google Cloud Document AI processor.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/batch-process-documents-with-processor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/batch-process-documents-with-processor?connectionId=$CONNECTION_ID&processorsId=string&inputDocuments=%5Bobject%20Object%5D&documentOutputConfig=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processorsId": "string",
  "inputDocuments": "[object Object]",
  "documentOutputConfig": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/batch-process-documents-with-processor?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processorsId` | string | yes | Document AI processor ID. |
| `inputDocuments` | object | yes | Batch input document source configuration. |
| `documentOutputConfig` | object | yes | Output destination for batch processing results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skipHumanReview` | boolean | no | Whether to skip human review. |
| `processOptions` | object | no | Optional processing configuration. |
| `labels` | object | no | Request labels to attach to processing metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:batchProcess` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-process-documents-with-processor.md) for the provider-specific parameters and requirements.

