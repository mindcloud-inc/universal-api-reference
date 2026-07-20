# Groq: Create Response

Creates a response in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes |  |
| `input` | string | yes |  |
| `instructions` | string | no |  |
| `metadata` | object | no |  |
| `parallelToolCalls` | boolean | no |  |
| `serviceTier` | list | no |  |
| `store` | boolean | no |  |
| `topP` | number | no |  |
| `truncation` | list | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxOutputTokens` | number | no |  |
| `temperature` | number | no |  |
| `stream` | boolean | no |  |
| `user` | string | no |  |
| `reasoningEffort` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": true,
      "createdAt": 1,
      "error": {},
      "id": "string",
      "incompleteDetails": {},
      "instructions": "string",
      "maxOutputTokens": 1,
      "metadata": {},
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "annotations": [
                "string"
              ],
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
      "previousResponseId": "string",
      "reasoning": {
        "effort": "string"
      },
      "serviceTier": "string",
      "status": "string",
      "store": true,
      "temperature": 1,
      "text": {
        "format": {
          "type": "string"
        }
      },
      "toolChoice": "string",
      "tools": [
        "string"
      ],
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
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | boolean |  |
| `createdAt` | number |  |
| `error` | object |  |
| `id` | string |  |
| `incompleteDetails` | object |  |
| `instructions` | string |  |
| `maxOutputTokens` | number |  |
| `metadata` | object |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].annotations` | array |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].id` | string |  |
| `output[].role` | string |  |
| `output[].status` | string |  |
| `output[].type` | string |  |
| `parallelToolCalls` | boolean |  |
| `previousResponseId` | string |  |
| `reasoning.effort` | string |  |
| `serviceTier` | string |  |
| `status` | string |  |
| `store` | boolean |  |
| `temperature` | number |  |
| `text.format.type` | string |  |
| `toolChoice` | string |  |
| `tools` | array |  |
| `topP` | number |  |
| `truncation` | string |  |
| `usage.inputTokens` | number |  |
| `usage.inputTokensDetails.cachedTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.outputTokensDetails.reasoningTokens` | number |  |
| `usage.totalTokens` | number |  |
| `user` | string |  |

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/responses` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

