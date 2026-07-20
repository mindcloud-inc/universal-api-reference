# LionWheel Delivery Universal API Examples

These examples use the MindCloud API key and LionWheel Delivery connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Tasks by Order ID

Finds tasks in LionWheel Delivery by order ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-order-id?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-order-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Find Tasks by Order ID action reference](actions/find-tasks-by-order-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lionWheelDelivery/latest/actions/find-tasks-by-order-id).

## Create Task

Creates a new task in LionWheel Delivery.

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

Example response:

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

See the full [Create Task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lionWheelDelivery/latest/actions/create-task).
