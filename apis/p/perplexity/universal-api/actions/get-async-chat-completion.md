# Perplexity: Get Async Chat Completion

Retrieves an async chat completion from Perplexity.

```
GET https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/get-async-chat-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/get-async-chat-completion?connectionId=$CONNECTION_ID&apiRequest=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiRequest": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/get-async-chat-completion?${params}`, {
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
| `apiRequest` | string | yes | Async request ID to retrieve. |

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

Through the native Perplexity API, this operation is `GET /v1/async/sonar/:api_request` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-chat-completion.md) for the provider-specific parameters and requirements.

