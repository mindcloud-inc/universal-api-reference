# vPlan: Create Stage



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "string",
  "delayDay": 1,
  "name": "Ava Chen",
  "priority": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-stage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "string",
    "delayDay": 1,
    "name": "Ava Chen",
    "priority": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | Board identifier for the new stage. |
| `delayDay` | number | yes | Stage delay day value. |
| `name` | string | yes | Stage name. |
| `priority` | number | yes | Stage priority. |

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
      "efficiency": 1,
      "id": "string",
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
| `efficiency` | number | Stage efficiency percentage. |
| `id` | string | Stage identifier. |
| `name` | string | Stage name. |
| `priority` | number | Stage priority. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `POST /stage` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-stage.md) for the provider-specific parameters and requirements.

