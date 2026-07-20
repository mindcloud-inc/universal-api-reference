# PromptLayer Run Agent: Get Request

Retrieves a request from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-request?connectionId=$CONNECTION_ID&requestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-request?${params}`, {
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
| `requestId` | number | yes | PromptLayer request ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inputTokens": 1,
      "latencyMs": 1,
      "model": "string",
      "outputTokens": 1,
      "price": 1,
      "promptBlueprint": {},
      "provider": "string",
      "requestEndTime": "string",
      "requestId": 1,
      "requestStartTime": "string",
      "success": true,
      "tokens": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inputTokens` | number |  |
| `latencyMs` | number |  |
| `model` | string |  |
| `outputTokens` | number |  |
| `price` | number |  |
| `promptBlueprint` | object |  |
| `provider` | string |  |
| `requestEndTime` | string |  |
| `requestId` | number |  |
| `requestStartTime` | string |  |
| `success` | boolean |  |
| `tokens` | number |  |
| `traceId` | string |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/requests/:request_id` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request.md) for the provider-specific parameters and requirements.

