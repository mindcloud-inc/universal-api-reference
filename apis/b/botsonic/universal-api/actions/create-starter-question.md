# Botsonic: Create Starter Question

Creates a new starter question in Botsonic.

```
POST https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-starter-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-starter-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "question": "What can you help with?",
  "answer": "I can answer questions about this business."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-starter-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "question": "What can you help with?",
    "answer": "I can answer questions about this business."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `question` | string | yes | Starter question text. Example: `What can you help with?`. |
| `answer` | string | yes | Answer shown for the starter question. Example: `I can answer questions about this business.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | number | no | Display order. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "bot_id": "string",
      "created_at": "string",
      "id": "string",
      "order": 1,
      "question": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Starter question answer. |
| `bot_id` | string | Bot identifier. |
| `created_at` | string | Creation timestamp. |
| `id` | string | Starter question identifier. |
| `order` | number | Display order. |
| `question` | string | Starter question text. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/bot-starter-questions` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-starter-question.md) for the provider-specific parameters and requirements.

