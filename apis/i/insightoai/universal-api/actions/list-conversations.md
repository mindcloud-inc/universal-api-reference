# Insighto.ai: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0&dateFrom=2026-03-01&dateTo=2026-03-30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dateFrom": "2026-03-01",
  "dateTo": "2026-03-30"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-conversations?${params}`, {
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
| `dateFrom` | string | yes | Start date in ISO format (YYYY-MM-DD). Example: `2026-03-01`. |
| `dateTo` | string | yes | End date in ISO format (YYYY-MM-DD). Example: `2026-03-30`. |
| `assistantId` | string | no | Filter conversations by assistant id. Example: `019d3ea9-2ce3-7bab-99d5-2676d463c293`. |
| `intentId` | string | no | Filter conversations by intent id. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `includesVoice` | boolean | no | Whether to include voice conversations. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant_id": "string",
      "assistant_name": "Ava Chen",
      "attributes": "string",
      "chat_count": 1,
      "contact_first_name": "Ava",
      "contact_id": "string",
      "contact_last_name": "Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "first_message": "string",
      "id": "string",
      "includes_voice": true,
      "intent_name": "Ava Chen",
      "summary": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "widget_id": "string",
      "widget_provider": "string",
      "widget_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistant_id` | string |  |
| `assistant_name` | string |  |
| `attributes` | string |  |
| `chat_count` | number |  |
| `contact_first_name` | string |  |
| `contact_id` | string |  |
| `contact_last_name` | string |  |
| `created_at` | date |  |
| `device_type` | string |  |
| `first_message` | string |  |
| `id` | string |  |
| `includes_voice` | boolean |  |
| `intent_name` | string |  |
| `summary` | string |  |
| `updated_at` | date |  |
| `widget_id` | string |  |
| `widget_provider` | string |  |
| `widget_type` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /conversation` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

