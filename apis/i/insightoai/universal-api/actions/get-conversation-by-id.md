# Insighto.ai: Get Conversation By Id



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-conversation-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-conversation-by-id?connectionId=$CONNECTION_ID&conversationId=3c90c3cc-0d44-4b50-8888-8dd25736052a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-conversation-by-id?${params}`, {
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
| `conversationId` | string | yes | The UUID id of the conversation. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant_id": "string",
      "attributes": {},
      "chat_count": 1,
      "contact_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "first_message": "string",
      "id": "string",
      "unique_device_id": "string",
      "widget_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistant_id` | string |  |
| `attributes` | object |  |
| `chat_count` | number |  |
| `contact_id` | string |  |
| `created_at` | date |  |
| `device_type` | string |  |
| `first_message` | string |  |
| `id` | string |  |
| `unique_device_id` | string |  |
| `widget_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /conversation/:conversation_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-by-id.md) for the provider-specific parameters and requirements.

