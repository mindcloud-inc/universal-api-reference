# LionWheel Delivery: Update Task

Updates an existing task in LionWheel Delivery.

```
PUT https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LionWheel Delivery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pickupAt` | string | no | Pickup date for the task. |
| `taskId` | string | yes | The LionWheel task ID. |
| `status` | number | no | Task status code: UNASSIGNED=0, ASSIGNED=1, ACTIVE=2, COMPLETED=3, CANCELED=4, ROUNDTRIP_DELIVERED=5, FAILED=8. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Mutation result message. |

## Native endpoint

Through the native LionWheel Delivery API, this operation is `PUT /tasks/:task_id/update` (base URL `https://test.lionwheel.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

