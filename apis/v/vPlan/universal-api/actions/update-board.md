# vPlan: Update Board



```
PUT https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "9a600586-cf12-4917-9f9e-49a931b50b69",
  "name": "Codex Action Board Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-board', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "9a600586-cf12-4917-9f9e-49a931b50b69",
    "name": "Codex Action Board Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Board identifier. Default: `9a600586-cf12-4917-9f9e-49a931b50b69`. |
| `name` | string | yes | Board name. Default: `Codex Action Board Updated`. |

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
      "custom_fields": [
        {}
      ],
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
| `custom_fields` | array<object> | Board custom fields. |
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

Through the native vPlan API, this operation is `PUT /board/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-board.md) for the provider-specific parameters and requirements.

