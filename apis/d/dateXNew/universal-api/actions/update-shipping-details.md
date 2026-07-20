# DateX: Update Shipping Details



```
PUT https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipping-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipping-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target.shipmentId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipping-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target.shipmentId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target.shipmentId` | number | yes | Shipment ID whose shipping details should be updated. Example: `12345`. |
| `change.shipment.trackingNumber` | string | no | Updated shipment tracking number. Example: `1Z999AA10123456784`. |
| `change.shipment.carrier` | string | no | Updated shipment carrier. Example: `UPS`. |
| `change.shipment.carrierService` | string | no | Updated shipment carrier service. Example: `Ground`. |
| `change.shippingContainers[]` | array<object> | no | Array of shipping container update objects, each including the documented container id and changed fields. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipmentId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipmentId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native DateX API, this operation is `POST shipments/shipping_details/update` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipping-details.md) for the provider-specific parameters and requirements.

