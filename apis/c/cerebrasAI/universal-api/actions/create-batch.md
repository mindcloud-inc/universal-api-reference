# Cerebras AI: Create Batch

Creates a batch in Cerebras AI.

```
POST https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputFileId": "string",
  "endpoint": "string",
  "completionWindow": "24h"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputFileId": "string",
    "endpoint": "string",
    "completionWindow": "24h"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputFileId` | string | yes |  |
| `endpoint` | string | yes |  |
| `completionWindow` | string | yes | Default: `24h`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionWindow": "string",
      "createdAt": 1,
      "endpoint": "string",
      "id": "string",
      "inputFileId": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completionWindow` | string |  |
| `createdAt` | number |  |
| `endpoint` | string |  |
| `id` | string |  |
| `inputFileId` | string |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `POST /v1/batches` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

