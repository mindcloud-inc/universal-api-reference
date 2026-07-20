# Easy-Peasy.AI: Generate Text

Generates text in Easy-Peasy.AI from a preset.

```
POST https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "preset": "string",
  "keywords": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "preset": "string",
    "keywords": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preset` | string | yes | The preset slug or identifier used for text generation. |
| `keywords` | string | yes | The prompt keywords or source text used to generate output. |
| `tone` | string | no | Optional tone to apply to the generated text. |
| `length` | string | no | Optional output length preference. |
| `outputs` | number | no | Optional number of generated outputs to return. |
| `language` | string | no | Optional target language for generated text. |
| `shouldUseGpt4` | boolean | no | Use the GPT-4 generation path when supported. |
| `suffix` | string | no | Optional suffix appended to the generated output. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `POST /api/generate` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-text.md) for the provider-specific parameters and requirements.

