# Heymarket SMS: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1&filters=%5Bobject%20Object%5D&filters.inboxes%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1",
  "filters": "[object Object]",
  "filters.inboxes[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-conversations?${params}`, {
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
| `id` | number | yes | User ID used to validate inbox access. |
| `filters` | object | yes | Conversation filters. |
| `filters.inboxes[]` | array<number> | yes | Inbox IDs to include. |
| `filters.closed` | boolean | no | Filter by closed conversations. |
| `filters.unread` | boolean | no | Filter by unread conversations for the given user. |
| `date` | date | no | Last updated timestamp for pagination. |

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
      "last_msg": "string",
      "local_id": "string",
      "members": [
        {}
      ],
      "muted": true,
      "op": "string",
      "read": 1,
      "replied": true,
      "status": "string",
      "super": 1,
      "target": "string",
      "unread": true,
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
| `last_msg` | string |  |
| `local_id` | string |  |
| `members` | array<object> |  |
| `muted` | boolean |  |
| `op` | string |  |
| `read` | number |  |
| `replied` | boolean |  |
| `status` | string |  |
| `super` | number |  |
| `target` | string |  |
| `unread` | boolean |  |
| `updated` | date |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/conversations` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

