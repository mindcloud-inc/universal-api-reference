# Document AI: Start Document Fields and Tables Batch Job

Creates a document extraction batch job in Document AI.

```
POST https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-fields-and-tables-batch-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-fields-and-tables-batch-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "InputFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-fields-and-tables-batch-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "InputFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `InputFile` | file | yes | Document file for the batch fields and tables extraction job. |

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

Through the native Document AI API, this operation is `POST /document-ai/document/batch-job/extract/all` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-document-fields-and-tables-batch-job.md) for the provider-specific parameters and requirements.

