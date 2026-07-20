# Botsonic: Get Conversation

Retrieves a specific conversation from Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-conversation?connectionId=$CONNECTION_ID&chatId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-conversation?${params}`, {
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
| `chatId` | string | yes | chat_id of the conversation. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "additional_feedback": "string",
      "bot_id": "string",
      "chat_data": [
        {}
      ],
      "chat_ended": true,
      "chat_id": "string",
      "chat_user": {},
      "created_at": "string",
      "ip_address": "string",
      "is_resolved": true,
      "num_messages": 1,
      "oai_thread_id": "string",
      "owner_id": "string",
      "source": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Internal conversation identifier. |
| `additional_feedback` | string | Additional feedback. |
| `bot_id` | string | Bot identifier. |
| `chat_data` | array<object> | Conversation messages and data. |
| `chat_ended` | boolean | Whether the chat ended. |
| `chat_id` | string | Conversation chat ID. |
| `chat_user` | object | Chat user details. |
| `created_at` | string | Creation timestamp. |
| `ip_address` | string | User IP address. |
| `is_resolved` | boolean | Whether the conversation is resolved. |
| `num_messages` | number | Number of messages. |
| `oai_thread_id` | string | OpenAI thread identifier. |
| `owner_id` | string | Owner identifier. |
| `source` | string | Conversation source. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot-data/conversations/:chatId` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

