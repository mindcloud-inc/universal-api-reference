# PromptLayer Run Agent: Log Request

Logs a request in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/log-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/log-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "provider": "string",
  "model": "string",
  "input": "[object Object]",
  "output": "[object Object]",
  "requestStartTime": "2026-04-24T17:10:00Z",
  "requestEndTime": "2026-04-24T17:10:01Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/log-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "provider": "string",
    "model": "string",
    "input": "[object Object]",
    "output": "[object Object]",
    "requestStartTime": "2026-04-24T17:10:00Z",
    "requestEndTime": "2026-04-24T17:10:01Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `provider` | string | yes | LLM provider for the logged request. |
| `model` | string | yes | Model name for the logged request. |
| `input` | object | yes | Prompt blueprint input payload. Example: `[object Object]`. |
| `output` | object | yes | Prompt blueprint output payload. Example: `[object Object]`. |
| `requestStartTime` | date | yes | ISO timestamp for when the request started. Example: `2026-04-24T17:10:00Z`. |
| `requestEndTime` | date | yes | ISO timestamp for when the request finished. Example: `2026-04-24T17:10:01Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiType` | string | no | Provider API type such as chat-completions. Example: `chat-completions`. |
| `metadata` | object | no | Optional metadata for request search and tracking. |
| `tags[]` | array<string> | no | Optional request tags. |
| `parameters` | object | no | Optional model parameters including structured outputs and reasoning settings. |
| `status` | list | no | Request status. Default: `SUCCESS`. |
| `errorType` | list | no | Optional categorized error type. |
| `errorMessage` | string | no | Optional detailed error message. |
| `promptInputVariables` | object | no | Input variables for the associated prompt template. |
| `inputTokens` | number | no | Number of input tokens used by the request. |
| `outputTokens` | number | no | Number of output tokens used by the request. |
| `price` | number | no | USD cost for the request. |
| `functionName` | string | no | Optional function name for the logged request. |
| `score` | number | no | Optional request score from 0 to 100. |
| `promptName` | string | no | Optional prompt template name associated with the request. |
| `promptId` | number | no | Optional prompt template ID associated with the request. |
| `promptVersionNumber` | number | no | Optional prompt version number associated with the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiType": "string",
      "engine": "string",
      "id": 1,
      "inputTokens": 1,
      "metadata": [
        {}
      ],
      "outputTokens": 1,
      "price": 1,
      "promptString": "string",
      "promptVersion": {},
      "providerType": "string",
      "requestEndTime": "string",
      "requestStartTime": "string",
      "responseString": "string",
      "status": "string",
      "tokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiType` | string |  |
| `engine` | string |  |
| `id` | number |  |
| `inputTokens` | number |  |
| `metadata` | array<object> |  |
| `outputTokens` | number |  |
| `price` | number |  |
| `promptString` | string |  |
| `promptVersion` | object |  |
| `providerType` | string |  |
| `requestEndTime` | string |  |
| `requestStartTime` | string |  |
| `responseString` | string |  |
| `status` | string |  |
| `tokens` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /log-request` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-request.md) for the provider-specific parameters and requirements.

