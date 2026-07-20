# Amazon Seller: Update Shipment Status

Updates shipment status for an Amazon Seller order.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-shipment-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-shipment-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "marketplaceID": "string",
  "orderId": "string",
  "shipmentStatus": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-shipment-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "marketplaceID": "string",
    "orderId": "string",
    "shipmentStatus": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `marketplaceID` | list<string> | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `orderItems[].orderItemId` | string | no | The order item's unique identifier. |
| `orderId` | string | yes | An Amazon-defined order identifier, in 3-7-7 format. |
| `orderItems[].quantity` | number | no | The quantity for which to update the shipment status. |
| `shipmentStatus` | list<string> | yes | The shipment status to apply. |
| `orderItems[]` | array<object> | no | For partial shipment status updates, provide a list of order items and quantities to be updated. Leave blank to apply the new status to the entire order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": "string",
      "shipmentStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | string | Amazon order identifier whose shipment status was updated. |
| `shipmentStatus` | string | Updated shipment status. |

## Native endpoint

Through the native Amazon Seller API, this operation is `POST orders/v0/orders/:orderId/shipment` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment-status.md) for the provider-specific parameters and requirements.

