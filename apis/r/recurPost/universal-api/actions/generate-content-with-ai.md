# RecurPost: Generate Content with AI

Generates social content with AI in RecurPost.

```
POST https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-content-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-content-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "promptText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-content-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "promptText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aiId` | string | no | AI session ID for continuing a previous conversation. |
| `chatHistory[]` | array<object> | no | Previous conversation messages with roles and content. |
| `chatProgress` | string | no | Progress marker returned by a previous AI response. |
| `promptText` | string | yes | Topic or text to generate content about. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_id": "string",
      "chat_progress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_id` | string |  |
| `chat_progress` | string |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/generate_content_with_ai` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-content-with-ai.md) for the provider-specific parameters and requirements.

