# Google Cloud Document AI: Process Document With Processor

Processes a document with a Google Cloud Document AI processor.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/process-document-with-processor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/process-document-with-processor?connectionId=$CONNECTION_ID&processorsId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processorsId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/process-document-with-processor?${params}`, {
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
| `rawDocument` | object | no | Raw document input, including content and MIME type. |
| `gcsDocument` | object | no | Google Cloud Storage document input. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inlineDocument` | object | no | Inline Document AI document object. |
| `skipHumanReview` | boolean | no | Whether to skip human review for this request. |
| `fieldMask` | string | no | Field mask selecting which document fields to return. |
| `processOptions` | object | no | Optional processing configuration. |
| `labels` | object | no | Request labels to attach to processing metadata. |
| `imagelessMode` | boolean | no | Whether to omit image content from the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:process` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-document-with-processor.md) for the provider-specific parameters and requirements.

