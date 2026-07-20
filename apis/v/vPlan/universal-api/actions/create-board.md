# vPlan: Create Board



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Board name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "capacity_method": "string",
      "card_lock_options": [
        "string"
      ],
      "color": "string",
      "created_at": "string",
      "deleted_at": "string",
      "dependency_behavior": "string",
      "id": "string",
      "name": "Ava Chen",
      "own_backlog": true,
      "permission_set": "string",
      "split_cards_by_activity": true,
      "updated_at": "string",
      "visibility": "string",
      "workdays": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string | Archive timestamp. |
| `capacity_method` | string | Capacity calculation method. |
| `card_lock_options` | array<string> | Card lock option list. |
| `color` | string | Board color. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp. |
| `dependency_behavior` | string | Dependency behavior. |
| `id` | string | Board identifier. |
| `name` | string | Board name. |
| `own_backlog` | boolean | Whether the board uses its own backlog. |
| `permission_set` | string | Permission set for the current auth. |
| `split_cards_by_activity` | boolean | Whether cards are split by activity. |
| `updated_at` | string | Last update timestamp. |
| `visibility` | string | Board visibility. |
| `workdays` | object | Configured workdays map. |

## Native endpoint

Through the native vPlan API, this operation is `POST /board` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-board.md) for the provider-specific parameters and requirements.

