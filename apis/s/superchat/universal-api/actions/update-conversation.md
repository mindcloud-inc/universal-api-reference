# Superchat: Update Conversation

Updates an existing conversation in Superchat.

```
PUT https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | The `id` of the conversation |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | The status of the conversation. |
| `snoozed_until` | date | no | Timestamp in UTC until when conversation is snoozed. |
| `assigned_users[]` | array<string> | no | Array of user_ids |
| `labels[]` | array<string> | no | Array of label_ids |
| `inbox_id` | string | no | Unique identifier of the inbox. Always bears prefix 'ib_' |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_users": {
        "email": "ava@example.com",
        "id": "string",
        "url": "https://example.com"
      },
      "channel": {
        "id": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "contacts": {
        "id": "string",
        "url": "https://example.com"
      },
      "id": "string",
      "inbox": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "labels": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "snoozed_until": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "time_window": {
        "open_until": "2026-05-07T12:00:00.000Z",
        "state": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_users` | array<object> |  |
| `assigned_users.email` | string |  |
| `assigned_users.id` | string |  |
| `assigned_users.url` | string |  |
| `channel` | object |  |
| `channel.id` | string |  |
| `channel.type` | string |  |
| `channel.url` | string |  |
| `contacts` | array<object> |  |
| `contacts.id` | string |  |
| `contacts.url` | string |  |
| `id` | string |  |
| `inbox` | object |  |
| `inbox.id` | string |  |
| `inbox.name` | string |  |
| `inbox.url` | string |  |
| `labels` | array<object> |  |
| `labels.id` | string |  |
| `labels.name` | string |  |
| `labels.url` | string |  |
| `snoozed_until` | date |  |
| `status` | string |  |
| `time_window` | object |  |
| `time_window.open_until` | date |  |
| `time_window.state` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `PATCH /conversations/{conversation_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

