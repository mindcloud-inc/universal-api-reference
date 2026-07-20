# Document AI: Start Document Field Values Batch Job

Creates a document field extraction batch job in Document AI.

```
POST https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-field-values-batch-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-field-values-batch-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "InputFile": "string",
  "FieldsToExtract[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-field-values-batch-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "InputFile": "string",
    "FieldsToExtract[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `InputFile` | string | yes | Base64-encoded document content for the batch field extraction job. |
| `FieldsToExtract[]` | array<object> | yes | Fields to extract from the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Recognition mode sent as the Cloudmersive recognitionMode header. Default: `Advanced`. |
| `MaximumPagesProcessed` | number | no | Maximum number of pages to process. |
| `Preprocessing` | string | no | Optional preprocessing mode. |
| `ResultCrossCheck` | string | no | Optional result cross-check mode. |
| `RotateImageDegrees` | number | no | Optional image rotation in degrees. |

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

Through the native Document AI API, this operation is `POST /document-ai/document/batch-job/extract/fields/advanced` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-document-field-values-batch-job.md) for the provider-specific parameters and requirements.

