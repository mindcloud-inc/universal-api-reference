# LionWheel Delivery: Create Task

Creates a new task in LionWheel Delivery.

```
POST https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LionWheel Delivery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "originalOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "originalOrderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationPhone` | string | no | The destination recipient phone number. |
| `notes` | string | no | General delivery notes. |
| `originalOrderId` | string | yes | Your external order ID for the task. |
| `pickupAt` | string | no | Pickup date in LionWheel's expected format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "destinationRegionStr": "string",
      "label": "string",
      "originalOrderId": "string",
      "publicId": "string",
      "taskId": 1,
      "trackingLink": "https://example.com",
      "waybill": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string | Task barcode. |
| `destinationRegionStr` | string | Destination region when available. |
| `label` | string | Printable label URL. |
| `originalOrderId` | string | External order ID supplied on create. |
| `publicId` | string | Public identifier for the created task. |
| `taskId` | number | Created LionWheel task ID. |
| `trackingLink` | string | Tracking URL for the created task. |
| `waybill` | string | Waybill URL. |

## Native endpoint

Through the native LionWheel Delivery API, this operation is `POST /tasks/create` (base URL `https://test.lionwheel.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

