# vPlan: Update Stage



```
PUT https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "bf97f40c-bd8c-4141-aa02-f9c267939b88",
  "name": "Codex Action Stage Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/update-stage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "bf97f40c-bd8c-4141-aa02-f9c267939b88",
    "name": "Codex Action Stage Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Stage identifier. Default: `bf97f40c-bd8c-4141-aa02-f9c267939b88`. |
| `name` | string | yes | Stage name. Default: `Codex Action Stage Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board_id": "string",
      "capacity_notification": true,
      "capacity_notification_max": 1,
      "capacity_notification_min": 1,
      "created_at": "string",
      "default_percentage": 1,
      "delay_day": 1,
      "deleted_at": "string",
      "efficiency": 1,
      "id": "string",
      "independent": true,
      "name": "Ava Chen",
      "priority": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board_id` | string | Board identifier. |
| `capacity_notification` | boolean | Whether capacity notifications are enabled. |
| `capacity_notification_max` | number | Maximum notification threshold. |
| `capacity_notification_min` | number | Minimum notification threshold. |
| `created_at` | string | Creation timestamp. |
| `default_percentage` | number | Default percentage allocation. |
| `delay_day` | number | Delay day value. |
| `deleted_at` | string | Deletion timestamp. |
| `efficiency` | number | Stage efficiency percentage. |
| `id` | string | Stage identifier. |
| `independent` | boolean | Whether this stage is independent. |
| `name` | string | Stage name. |
| `priority` | number | Stage priority. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `PUT /stage/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-stage.md) for the provider-specific parameters and requirements.

