# Superchat: List Conversations

Retrieves conversations from a Superchat workspace.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-conversations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Specify the cursor before which objects should be returned. |

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

Through the native Superchat API, this operation is `GET /conversations` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

