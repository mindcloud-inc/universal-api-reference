# Walmart: Get Inbound Shipment Items

Retrieve a list of inbound shipments with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-items?connectionId=$CONNECTION_ID&limit=25&offset=0&shipmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shipmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-items?${params}`, {
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
| `shipmentId` | string | yes | Unique ID identifying each shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "damagedQty": 1,
      "expectedDeliveryDate": "string",
      "fillRate": 1,
      "gtin": "string",
      "inboundOrderId": "string",
      "innerPackQty": 1,
      "itemDesc": "string",
      "itemQty": 1,
      "receivedQty": 1,
      "shipmentId": "string",
      "shipNodeName": "Ava Chen",
      "sku": "string",
      "updatedExpectedDeliveryDate": "string",
      "vendorPackQty": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `damagedQty` | number |  |
| `expectedDeliveryDate` | string |  |
| `fillRate` | number |  |
| `gtin` | string |  |
| `inboundOrderId` | string |  |
| `innerPackQty` | number |  |
| `itemDesc` | string |  |
| `itemQty` | number |  |
| `receivedQty` | number |  |
| `shipmentId` | string |  |
| `shipNodeName` | string |  |
| `sku` | string |  |
| `updatedExpectedDeliveryDate` | string |  |
| `vendorPackQty` | number |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/fulfillment/inbound-shipment-items` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-inbound-shipment-items.md) for the provider-specific parameters and requirements.

