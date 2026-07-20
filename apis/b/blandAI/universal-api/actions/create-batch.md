# Bland AI: Create Batch

Creates a new call batch in Bland AI.

```
POST https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "global": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "global": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callObjects[]` | array<string> | no |  |
| `global` | object | yes |  |
| `statusWebhook` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v2/batches/create` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

