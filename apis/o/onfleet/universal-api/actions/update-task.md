# Onfleet: Update Task

Updates an existing task in Onfleet.

```
PUT https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-task', {
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
| `taskId` | string | yes | The Onfleet task ID. |
| `destination` | string | no | The ID of the updated destination. |
| `notes` | string | no | Updated notes for the task. |
| `container.type` | string | no | The container type for the updated task container. |
| `container.team` | string | no | The team ID when moving the task into a team container. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completeAfter": 1,
      "completeBefore": 1,
      "container": {},
      "destination": {},
      "id": "string",
      "notes": "string",
      "pickupTask": true,
      "quantity": 1,
      "recipients": [
        {}
      ],
      "serviceTime": 1,
      "shortId": "string",
      "state": 1,
      "trackingURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeAfter` | number |  |
| `completeBefore` | number |  |
| `container` | object |  |
| `destination` | object |  |
| `id` | string |  |
| `notes` | string |  |
| `pickupTask` | boolean |  |
| `quantity` | number |  |
| `recipients` | array<object> |  |
| `serviceTime` | number |  |
| `shortId` | string |  |
| `state` | number |  |
| `trackingURL` | string |  |

## Native endpoint

Through the native Onfleet API, this operation is `PUT /tasks/:taskId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

