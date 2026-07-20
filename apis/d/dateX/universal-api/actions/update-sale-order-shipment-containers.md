# DateX (Legacy): Update sale order shipment containers

Just the markup value, status gets updated automatically

```
PUT https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-sale-order-shipment-containers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-sale-order-shipment-containers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target": {},
  "change": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-sale-order-shipment-containers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target": {},
    "change": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `change.shipment` | object | no |  |
| `change.shipment.tracking_number` | string | no |  |
| `change.shipping_containers[].id` | number | no |  |
| `target` | object | yes |  |
| `target.shipment_id` | number | no |  |
| `change` | object | yes |  |
| `change.shipping_containers[]` | array<object> | no |  |
| `change.shipping_containers[].tracking_number` | string | no |  |
| `change.shipment.carrier` | string | no |  |
| `change.shipping_containers[].length` | number | no |  |
| `change.shipment.carrier_service` | string | no |  |
| `change.shipping_containers[].width` | number | no |  |
| `change.shipping_containers[].height` | number | no |  |
| `change.shipping_containers[].dimension_uom` | string | no |  |
| `change.shipping_containers[].weight` | number | no |  |
| `change.shipping_containers[].weightUom` | string | no |  |
| `change.shipping_containers[].carrier` | string | no |  |
| `change.shipping_containers[].carrier_service` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DateX (Legacy) API returns.

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST shipments/shipping_details/update` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sale-order-shipment-containers.md) for the provider-specific parameters and requirements.

