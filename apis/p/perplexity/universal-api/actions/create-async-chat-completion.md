# Perplexity: Create Async Chat Completion

Creates an async chat completion in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-async-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-async-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-async-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | yes | Chat completion request object to execute asynchronously. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idempotencyKey` | string | no | Optional key to prevent duplicate async requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": 1,
      "created_at": 1,
      "error_message": "string",
      "failed_at": 1,
      "id": "string",
      "model": "string",
      "started_at": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | number |  |
| `created_at` | number |  |
| `error_message` | string |  |
| `failed_at` | number |  |
| `id` | string |  |
| `model` | string |  |
| `started_at` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /v1/async/sonar` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-chat-completion.md) for the provider-specific parameters and requirements.

