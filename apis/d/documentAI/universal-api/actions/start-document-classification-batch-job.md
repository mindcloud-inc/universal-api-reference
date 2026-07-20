# Document AI: Start Document Classification Batch Job

Creates a document classification batch job in Document AI.

```
POST https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-classification-batch-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-classification-batch-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "InputFile": "string",
  "Categories": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-classification-batch-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "InputFile": "string",
    "Categories": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `InputFile` | file | yes | Document file for the batch classification job. |
| `Categories` | string | yes | Comma-separated document categories sent as the Cloudmersive Categories header. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Optional recognition mode sent as a request header. Default: `Advanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncJobID": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncJobID` | string | Cloudmersive asynchronous job ID. |
| `successful` | boolean | Whether the batch job was started. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/batch-job/extract/classify` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-document-classification-batch-job.md) for the provider-specific parameters and requirements.

