# SuperSend: List Conversations

Retrieves conversations from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-conversations?${params}`, {
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
| `teamId` | string | no | Filter by team ID (UUID from list teams) |
| `channel` | string | no | Allowed values: email, linkedin, twitter. Default: linkedin. |
| `lastMessageDirection` | string | no | Allowed values: inbound, outbound. |
| `identityId` | string | no |  |
| `status` | string | no | Allowed values: archived, unarchived. |
| `readStatus` | string | no | Allowed values: read, unread. |
| `search` | string | no |  |
| `sortBy` | string | no | Sort field (default date) Allowed values: date. |
| `sortDirection` | string | no | Allowed values: asc, desc. Default: desc. |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "identity": {
        "first_name": "Ava",
        "handle": "string",
        "id": "string",
        "last_name": "Chen",
        "photo": "string",
        "type": "string"
      },
      "is_archived": true,
      "is_unread": true,
      "last_activity_at": "2026-05-07T12:00:00.000Z",
      "last_message": {
        "text": "string",
        "timestamp": "2026-05-07T12:00:00.000Z"
      },
      "object": "string",
      "participants": [
        {
          "avatar_url": "https://example.com",
          "display_name": "Ava Chen",
          "id": "string",
          "is_self": true,
          "username": "Ava Chen"
        }
      ],
      "platform_type": "string",
      "team_id": "string",
      "title": "string",
      "unread_count": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `identity.first_name` | string |  |
| `identity.handle` | string |  |
| `identity.id` | string |  |
| `identity.last_name` | string |  |
| `identity.photo` | string |  |
| `identity.type` | string |  |
| `is_archived` | boolean |  |
| `is_unread` | boolean |  |
| `last_activity_at` | date |  |
| `last_message.text` | string |  |
| `last_message.timestamp` | date |  |
| `object` | string |  |
| `participants[].avatar_url` | string |  |
| `participants[].display_name` | string |  |
| `participants[].id` | string |  |
| `participants[].is_self` | boolean |  |
| `participants[].username` | string |  |
| `platform_type` | string |  |
| `team_id` | string |  |
| `title` | string |  |
| `unread_count` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /conversations` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

