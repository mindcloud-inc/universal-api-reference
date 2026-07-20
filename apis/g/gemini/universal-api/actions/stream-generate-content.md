# Gemini: Stream Generate Content

Generates streamed content with a Gemini model.

```
POST https://connect.mindcloud.co/v1/universal/gemini/latest/actions/stream-generate-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/stream-generate-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gemini-2.5-flash:streamGenerateContent",
  "contents[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/stream-generate-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gemini-2.5-flash:streamGenerateContent",
    "contents[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Required. Model endpoint token including suffix, for example gemini-2.5-flash:streamGenerateContent. Example: `gemini-2.5-flash:streamGenerateContent`. |
| `contents[]` | array<object> | yes | Conversation content for the model. Required by Gemini. Example: `[object Object]`. |
| `systemInstruction` | object | no | Optional system-level instruction content. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generationConfig` | object | no | Optional generation controls such as temperature and max output tokens. Example: `[object Object]`. |
| `safetySettings[]` | array<object> | no | Optional safety thresholds by harm category. Example: `[object Object]`. |
| `tools[]` | array<object> | no | Optional tool declarations available to the model. Example: `[object Object]`. |
| `toolConfig` | object | no | Optional tool execution configuration. Example: `[object Object]`. |
| `cachedContent` | string | no | Optional cached content resource to ground generation. Example: `cachedContents/abc123`. |

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
| `candidates` | array<object> | Model-generated candidate responses for each stream chunk. |
| `modelVersion` | string | Model version used for generation. |
| `promptFeedback` | object | Prompt-level safety and block feedback. |
| `usageMetadata` | object | Token accounting and request usage metadata. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-generate-content.md) for the provider-specific parameters and requirements.

