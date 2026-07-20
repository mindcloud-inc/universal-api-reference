# Heymarket SMS: Get Conversation



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation?connectionId=$CONNECTION_ID&conversationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation?${params}`, {
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
| `conversationId` | number | yes | Unique identifier of the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned": 1,
      "blocked": true,
      "channel": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email_noti": true,
      "id": 1,
      "inbox": 1,
      "local_id": "string",
      "muted": true,
      "read": 1,
      "replied": true,
      "status": "string",
      "super": 1,
      "target": "string",
      "unread": true,
      "unread_users": [
        1
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned` | number |  |
| `blocked` | boolean |  |
| `channel` | string |  |
| `created` | date |  |
| `email_noti` | boolean |  |
| `id` | number |  |
| `inbox` | number |  |
| `local_id` | string |  |
| `muted` | boolean |  |
| `read` | number |  |
| `replied` | boolean |  |
| `status` | string |  |
| `super` | number |  |
| `target` | string |  |
| `unread` | boolean |  |
| `unread_users` | array<number> |  |
| `updated` | date |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/conversations/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

