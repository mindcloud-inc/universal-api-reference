# iPaymu: Calculate COD Shipping

Calculate shipping costs for an iPaymu cash-on-delivery shipment.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/calculate-cod-shipping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/calculate-cod-shipping?connectionId=$CONNECTION_ID&destination_area_id=string&pickup_area_id=string&weight=1&amount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destination_area_id": "string",
  "pickup_area_id": "string",
  "weight": "1",
  "amount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/calculate-cod-shipping?${params}`, {
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
| `destination_area_id` | string | yes | Destination area identifier. |
| `pickup_area_id` | string | yes | Pickup area identifier. |
| `weight` | number | yes | Shipment weight in kilograms. |
| `amount` | number | yes | Order amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "serviceName": "Ava Chen",
      "shippingFee": 1,
      "shippingName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string |  |
| `serviceName` | string |  |
| `shippingFee` | number |  |
| `shippingName` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /cod/shipping-calculate` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-cod-shipping.md) for the provider-specific parameters and requirements.

