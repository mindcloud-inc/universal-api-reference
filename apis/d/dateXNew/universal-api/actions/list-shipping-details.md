# DateX: List Shipping Details



```
GET https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-shipping-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-shipping-details?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-shipping-details?${params}`, {
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
| `filters.orderIds[]` | array<number> | no | Order ID filters. |
| `filters.orderLookups[]` | array<string> | no | Order lookup filters. |
| `filters.shipmentIds[]` | array<number> | no | Shipment ID filters. |
| `filters.shipmentLookups[]` | array<string> | no | Shipment lookup filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipment": {
        "carrier": "string",
        "carrierService": "string",
        "id": 1,
        "lookup": "string",
        "trackingNumber": "string"
      },
      "shippingContainers": [
        {
          "contents": [
            {}
          ],
          "dimensionUom": "string",
          "height": 1,
          "id": 1,
          "length": 1,
          "lookup": "string",
          "trackingNumber": "string",
          "weight": 1,
          "weightUom": "string",
          "width": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipment.carrier` | string |  |
| `shipment.carrierService` | string |  |
| `shipment.id` | number |  |
| `shipment.lookup` | string |  |
| `shipment.trackingNumber` | string |  |
| `shippingContainers[].contents` | array<object> |  |
| `shippingContainers[].dimensionUom` | string |  |
| `shippingContainers[].height` | number |  |
| `shippingContainers[].id` | number |  |
| `shippingContainers[].length` | number |  |
| `shippingContainers[].lookup` | string |  |
| `shippingContainers[].trackingNumber` | string |  |
| `shippingContainers[].weight` | number |  |
| `shippingContainers[].weightUom` | string |  |
| `shippingContainers[].width` | number |  |

## Native endpoint

Through the native DateX API, this operation is `POST shipments/shipping_details/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipping-details.md) for the provider-specific parameters and requirements.

