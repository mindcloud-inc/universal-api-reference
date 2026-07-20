# Open AI: Get Response

Retrieves a model response from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-response?connectionId=$CONNECTION_ID&response_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "response_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-response?${params}`, {
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
| `response_id` | string | yes | The ID of the response to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": true,
      "billing": {
        "payer": "string"
      },
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": {},
      "frequencyPenalty": 1,
      "id": "string",
      "incompleteDetails": "2026-05-07T12:00:00.000Z",
      "instructions": "2026-05-07T12:00:00.000Z",
      "maxOutputTokens": "2026-05-07T12:00:00.000Z",
      "maxToolCalls": "2026-05-07T12:00:00.000Z",
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "parallelToolCalls": true,
      "presencePenalty": 1,
      "previousResponseId": "2026-05-07T12:00:00.000Z",
      "promptCacheKey": "2026-05-07T12:00:00.000Z",
      "promptCacheRetention": {},
      "reasoning": {
        "effort": {},
        "summary": {}
      },
      "safetyIdentifier": {},
      "serviceTier": "string",
      "status": "string",
      "store": true,
      "temperature": "2026-05-07T12:00:00.000Z",
      "text": {
        "format": {
          "type": "string"
        },
        "verbosity": "string"
      },
      "toolChoice": "string",
      "topLogprobs": 1,
      "topP": 1,
      "truncation": "string",
      "usage": {
        "inputTokens": 1,
        "inputTokensDetails": {
          "cachedTokens": 1
        },
        "outputTokens": 1,
        "outputTokensDetails": {
          "reasoningTokens": 1
        },
        "totalTokens": 1
      },
      "user": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | boolean |  |
| `billing.payer` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `error` | object |  |
| `frequencyPenalty` | number |  |
| `id` | string |  |
| `incompleteDetails` | date |  |
| `instructions` | date |  |
| `maxOutputTokens` | date |  |
| `maxToolCalls` | date |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].id` | string |  |
| `output[].role` | string |  |
| `output[].status` | string |  |
| `output[].type` | string |  |
| `parallelToolCalls` | boolean |  |
| `presencePenalty` | number |  |
| `previousResponseId` | date |  |
| `promptCacheKey` | date |  |
| `promptCacheRetention` | object |  |
| `reasoning.effort` | object |  |
| `reasoning.summary` | object |  |
| `safetyIdentifier` | object |  |
| `serviceTier` | string |  |
| `status` | string |  |
| `store` | boolean |  |
| `temperature` | date |  |
| `text.format.type` | string |  |
| `text.verbosity` | string |  |
| `toolChoice` | string |  |
| `topLogprobs` | number |  |
| `topP` | number |  |
| `truncation` | string |  |
| `usage.inputTokens` | number |  |
| `usage.inputTokensDetails.cachedTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.outputTokensDetails.reasoningTokens` | number |  |
| `usage.totalTokens` | number |  |
| `user` | date |  |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/responses/:response_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response.md) for the provider-specific parameters and requirements.

