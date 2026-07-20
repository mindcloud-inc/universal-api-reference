# Google Cloud Document AI: Evaluate Processor Version

Evaluates a processor version in Google Cloud Document AI.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/evaluate-processor-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/evaluate-processor-version?connectionId=$CONNECTION_ID&processorsId=string&processorVersionsId=string&evaluationDocuments=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processorsId": "string",
  "processorVersionsId": "string",
  "evaluationDocuments": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/evaluate-processor-version?${params}`, {
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
| `processorVersionsId` | string | yes | Processor version ID. |
| `evaluationDocuments` | object | yes | Documents used to evaluate the processor version. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Document AI API returns.

## Native endpoint

Through the native Google Cloud Document AI API, this operation is `POST /v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:evaluateProcessorVersion` (base URL `https://documentai.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-processor-version.md) for the provider-specific parameters and requirements.

