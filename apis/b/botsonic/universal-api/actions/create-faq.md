# Botsonic: Create FAQ

Creates a new FAQ in Botsonic.

```
POST https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-faq
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-faq" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "question": "What is Botsonic?",
  "answer": "Botsonic is an AI chatbot platform."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/create-faq', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "question": "What is Botsonic?",
    "answer": "Botsonic is an AI chatbot platform."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `question` | string | yes | FAQ question. Example: `What is Botsonic?`. |
| `answer` | string | yes | FAQ answer. Example: `Botsonic is an AI chatbot platform.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "bot_id": "string",
      "characters": 1,
      "created_at": "string",
      "error_reason": "string",
      "id": "string",
      "migration_status": "string",
      "question": "string",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | FAQ answer. |
| `bot_id` | string | Bot identifier. |
| `characters` | number | Character count. |
| `created_at` | string | Creation timestamp. |
| `error_reason` | string | Processing error reason. |
| `id` | string | FAQ identifier. |
| `migration_status` | string | Migration status. |
| `question` | string | FAQ question. |
| `status` | string | FAQ processing status. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/bot-faq` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-faq.md) for the provider-specific parameters and requirements.

