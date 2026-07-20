# Extensiv Order Manager: List Shipments

Retrieves shipments from Extensiv Order Manager.

```
GET https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-shipments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-shipments?${params}`, {
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
| `batchNumber` | string | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `deliveryStatus` | list<string> | no |  |
| `orderId[]` | array<number> | no |  |
| `orderNumber[]` | array<string> | no |  |
| `recipient` | string | no |  |
| `salesChannelId` | number | no |  |
| `shipmentCreatedFromDate` | string | no |  |
| `shipmentCreatedToDate` | string | no |  |
| `shipmentFromDate` | string | no |  |
| `shipmentId[]` | array<number> | no |  |
| `shipmentToDate` | string | no |  |
| `shippingProviderId` | number | no |  |
| `state` | string | no |  |
| `trackingNumber` | string | no |  |
| `warehouseId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryStatus": "string",
      "orderId": 1,
      "orderNumber": "string",
      "shipDate": "2026-05-07T12:00:00.000Z",
      "shipmentId": 1,
      "trackingNumber": "string",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryStatus` | string | Delivery status. |
| `orderId` | number | Order identifier. |
| `orderNumber` | string | Order number. |
| `shipDate` | date | Shipment date. |
| `shipmentId` | number | Shipment identifier. |
| `trackingNumber` | string | Carrier tracking number. |
| `warehouseId` | number | Warehouse identifier. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `GET /v1/shipments` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

