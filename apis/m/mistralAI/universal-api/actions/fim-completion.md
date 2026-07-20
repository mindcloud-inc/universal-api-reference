# Mistral AI: FIM Completion

Creates a fill-in-the-middle completion in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/fim-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/fim-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/fim-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | ID of the model with FIM support to use. |
| `prompt` | string | yes | The text or code prefix to complete. |
| `suffix` | string | no | Optional suffix that the model should complete toward. |
| `temperature` | number | no | Sampling temperature for generation. |
| `topP` | number | no | Nucleus sampling cutoff. |
| `maxTokens` | number | no | Maximum number of tokens to generate. |
| `minTokens` | number | no | Minimum number of tokens to generate. |
| `stream` | boolean | no | Whether to stream partial progress. |
| `stop` | string | no | Stop generation when a token or one of the provided tokens is detected. |
| `randomSeed` | number | no | Seed to use for deterministic random sampling. |
| `metadata` | object | no | Optional metadata object for the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> |  |
| `created` | number |  |
| `id` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Mistral AI API, this operation is `POST /v1/fim/completions` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fim-completion.md) for the provider-specific parameters and requirements.

