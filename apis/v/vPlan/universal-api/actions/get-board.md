# vPlan: Get Board



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-board?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-board?${params}`, {
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
| `id` | string | yes | Board identifier. |

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

Through the native vPlan API, this operation is `GET /board/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board.md) for the provider-specific parameters and requirements.

