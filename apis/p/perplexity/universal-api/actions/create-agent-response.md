# Perplexity: Create Agent Response

Creates an agent response in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-agent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-agent-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-agent-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Input content. Perplexity also accepts array-form input items; this action currently models the common string input path. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | string | no | System instructions for the model. |
| `model` | string | no | Model ID in provider/model format. |
| `preset` | string | no | Preset configuration name such as fast-search or pro-search. |
| `maxOutputTokens` | number | no | Maximum tokens to generate. |
| `maxSteps` | number | no | Maximum research loop steps. |
| `stream` | boolean | no | When true, returns SSE events instead of JSON. |
| `languagePreference` | string | no | ISO 639-1 language code for the preferred response language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "id": "string",
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
          "role": "string",
          "type": "string"
        }
      ],
      "status": "string",
      "usage": {
        "input_tokens": 1,
        "output_tokens": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].role` | string |  |
| `output[].type` | string |  |
| `status` | string |  |
| `usage.input_tokens` | number |  |
| `usage.output_tokens` | number |  |
| `usage.total_tokens` | number |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /v1/agent` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-response.md) for the provider-specific parameters and requirements.

