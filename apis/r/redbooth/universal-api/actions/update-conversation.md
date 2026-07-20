# Redbooth: Update Conversation

Updates an existing conversation in Redbooth.

```
PUT https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Redbooth conversation ID |
| `name` | string | yes | Updated conversation title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments_count": 1,
      "created_at": 1,
      "id": 1,
      "is_private": true,
      "last_activity_id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "tag_ids": [
        1
      ],
      "updated_at": 1,
      "user_id": 1,
      "watcher_ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments_count` | number |  |
| `created_at` | number |  |
| `id` | number |  |
| `is_private` | boolean |  |
| `last_activity_id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `tag_ids` | array<number> |  |
| `updated_at` | number |  |
| `user_id` | number |  |
| `watcher_ids` | array<number> |  |

## Native endpoint

Through the native Redbooth API, this operation is `PUT /conversations/:id` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

