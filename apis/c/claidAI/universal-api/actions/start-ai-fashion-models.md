# Claid AI: Start AI Fashion Models

Starts AI fashion model generation in Claid AI.

```
POST https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/start-ai-fashion-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/start-ai-fashion-models" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {},
  "options": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/start-ai-fashion-models', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {},
    "options": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | object | yes |  |
| `options` | object | yes |  |
| `output` | string | no | Example: `storage://storage_1/output/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "request": {},
      "result_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Request creation timestamp. |
| `id` | number | Accepted task identifier. |
| `request` | object | Echoed request payload. |
| `result_url` | string | URL used to poll the async result. |
| `status` | string | Accepted processing status. |

## Native endpoint

Through the native Claid AI API, this operation is `POST image/ai-fashion-models` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-ai-fashion-models.md) for the provider-specific parameters and requirements.

