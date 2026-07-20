# Wodely: Create Tasks in Batch



```
POST https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-tasks-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-tasks-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tasks[].taskTypeId": "1",
  "tasks[].destinationAddress": "1600 Amphitheatre Parkway, Mountain View, CA 94043, USA"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-tasks-in-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tasks[].taskTypeId": "1",
    "tasks[].destinationAddress": "1600 Amphitheatre Parkway, Mountain View, CA 94043, USA"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks[].taskTypeId` | number | yes | 1: Delivery; 2: Pickup; 3: Appointment; 4: Field Workforce; 5: In-store Pickup; 6: Curbside Pickup; 7: Drive-thru Pickup. Example: `1`. |
| `tasks[].destinationAddress` | string | yes | Full delivery destination address. Example: `1600 Amphitheatre Parkway, Mountain View, CA 94043, USA`. |
| `tasks[].taskDesc` | string | no | Short description of the task. |
| `tasks[].requesterName` | string | no | Requester or sender name. |
| `tasks[].recipientName` | string | no | Destination recipient name. |
| `tasks[].recipientPhone` | string | no | Destination recipient phone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tasks[].externalKey` | string | no | External order Id or barcode. Example: `order-123`. |
| `tasks[].alert` | string | no | Set to N to disable notifications. Example: `N`. |
| `tasks[].afterDateTime` | string | no | Complete after time in UTC ISO 8601. Example: `2026-03-27T18:00:00Z`. |
| `tasks[].beforeDateTime` | string | no | Complete before time in UTC ISO 8601. Example: `2026-03-28T18:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert": "string",
      "assignedToDriverUserId": "string",
      "createdDateTime": "string",
      "destinationAddress": "string",
      "externalKey": "string",
      "guid": "string",
      "id": 1,
      "statusDesc": "string",
      "statusId": 1,
      "taskDesc": "string",
      "typeDesc": "string",
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert` | string |  |
| `assignedToDriverUserId` | string |  |
| `createdDateTime` | string |  |
| `destinationAddress` | string |  |
| `externalKey` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `statusDesc` | string |  |
| `statusId` | number |  |
| `taskDesc` | string |  |
| `typeDesc` | string |  |
| `typeId` | number |  |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/tasks/bulkcreate` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tasks-in-batch.md) for the provider-specific parameters and requirements.

