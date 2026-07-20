# Order Desk: Delete Shipment

Deletes an existing shipment from Order Desk.

```
DELETE https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-shipment?connectionId=$CONNECTION_ID&orderId=string&shipmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string",
  "shipmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-shipment?${params}`, {
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
| `orderId` | string | yes | Order Desk internal order ID. |
| `shipmentId` | string | yes | Order Desk internal shipment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `DELETE /orders/:orderId/shipments/:shipmentId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-shipment.md) for the provider-specific parameters and requirements.

