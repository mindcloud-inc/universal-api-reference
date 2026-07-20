# Order Desk: List Shipments

Retrieves shipments from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-shipments?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-shipments?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrierCode": "string",
      "cartShipmentId": "string",
      "cost": "string",
      "dateAdded": "string",
      "dateShipped": "string",
      "id": "string",
      "labelFormat": "string",
      "labelImage": "string",
      "labelShipmentId": "string",
      "orderId": "string",
      "orderItems": {},
      "printStatus": "string",
      "shipmentMethod": "string",
      "source": "string",
      "status": "string",
      "storeId": "string",
      "trackingNumber": "string",
      "trackingUrl": "https://example.com",
      "weight": "string",
      "weightUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierCode` | string |  |
| `cartShipmentId` | string |  |
| `cost` | string |  |
| `dateAdded` | string |  |
| `dateShipped` | string |  |
| `id` | string |  |
| `labelFormat` | string |  |
| `labelImage` | string |  |
| `labelShipmentId` | string |  |
| `orderId` | string |  |
| `orderItems` | object |  |
| `printStatus` | string |  |
| `shipmentMethod` | string |  |
| `source` | string |  |
| `status` | string |  |
| `storeId` | string |  |
| `trackingNumber` | string |  |
| `trackingUrl` | string |  |
| `weight` | string |  |
| `weightUnit` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `GET /orders/:orderId/shipments` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

