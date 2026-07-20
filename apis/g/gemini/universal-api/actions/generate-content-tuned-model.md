# Gemini: Generate Content (Tuned Model)

Generates content with a tuned model in Gemini.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/generate-content-tuned-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/generate-content-tuned-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "contents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/generate-content-tuned-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "contents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Tuned model token for this route. Use tuned model ID with operation suffix and no `tunedModels/` prefix (for example `my-model-id:generateContent`). |
| `contents[]` | array<object> | yes | Conversation content for the model. Required by Gemini. |
| `systemInstruction` | object | no | Optional system-level instruction content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generationConfig` | object | no | Optional generation controls such as temperature and max output tokens. |
| `safetySettings[]` | array<object> | no | Optional safety thresholds by harm category. |
| `tools[]` | array<object> | no | Optional tool declarations available to the model. |
| `toolConfig` | object | no | Optional tool execution configuration. |
| `cachedContent` | string | no | Optional cached content resource to ground generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidates": [
        {}
      ],
      "modelVersion": "string",
      "promptFeedback": {},
      "usageMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidates` | array<object> | Model-generated candidate responses. |
| `modelVersion` | string | Model version used for generation. |
| `promptFeedback` | object | Prompt-level safety and block feedback. |
| `usageMetadata` | object | Token accounting and request usage metadata. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/tunedModels/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-content-tuned-model.md) for the provider-specific parameters and requirements.

