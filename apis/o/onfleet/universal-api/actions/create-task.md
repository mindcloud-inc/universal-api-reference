# Onfleet: Create Task

Creates a new task in Onfleet.

```
POST https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | The ID of the task destination. |
| `recipients[]` | array<string> | no | An array containing zero or one recipient IDs. |
| `completeAfter` | number | no | Earliest completion time as a Unix timestamp in milliseconds. |
| `completeBefore` | number | no | Latest completion time as a Unix timestamp in milliseconds. |
| `pickupTask` | boolean | no | Whether the task is a pickup task. |
| `notes` | string | no | Optional notes for the task. |
| `quantity` | number | no | The number of units to be dropped off while completing this task. |
| `serviceTime` | number | no | The number of minutes a worker should spend on arrival at this task's destination. |
| `recipientName` | string | no | Optional recipient name override for this task only. |
| `recipientNotes` | string | no | Optional recipient notes override for this task only. |
| `recipientSkipSMSNotifications` | boolean | no | Optional recipient SMS notification override for this task only. |

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

Through the native Onfleet API, this operation is `POST /tasks` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

