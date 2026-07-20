# Unleashed: Create Sales Shipment

Creates a new sales shipment in Unleashed.

```
POST https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guid": "string",
  "orderNumber": "string",
  "shipmentStatus": "string",
  "salesShipmentLines[].product.productCode": "string",
  "salesShipmentLines[].shipmentQty": 1,
  "salesShipmentLines[].salesOrderLineNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guid": "string",
    "orderNumber": "string",
    "shipmentStatus": "string",
    "salesShipmentLines[].product.productCode": "string",
    "salesShipmentLines[].shipmentQty": 1,
    "salesShipmentLines[].salesOrderLineNumber": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guid` | string | yes | Unique identifier for the sales shipment. |
| `orderNumber` | string | yes | Order number for the sales shipment. |
| `shipmentStatus` | string | yes | Shipment status for the sales shipment. |
| `salesShipmentLines[].product.productCode` | string | yes | Product code for the sales shipment line. |
| `salesShipmentLines[].shipmentQty` | number | yes | Shipment quantity for the sales shipment line. |
| `salesShipmentLines[].salesOrderLineNumber` | number | yes | Sales order line number for the shipment line. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "createdOn": "string",
      "customer": {},
      "dispatchDate": "string",
      "guid": "string",
      "lastModifiedOn": "string",
      "orderGuid": "string",
      "orderNumber": "string",
      "salesShipmentLines": [
        {}
      ],
      "shipmentNumber": "string",
      "shipmentStatus": "string",
      "shipmentStatusEnum": 1,
      "shippingCompany": "string",
      "totalCommercialValue": 1,
      "trackingNumber": "string",
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `createdOn` | string |  |
| `customer` | object |  |
| `dispatchDate` | string |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `orderGuid` | string |  |
| `orderNumber` | string |  |
| `salesShipmentLines` | array<object> |  |
| `shipmentNumber` | string |  |
| `shipmentStatus` | string |  |
| `shipmentStatusEnum` | number |  |
| `shippingCompany` | string |  |
| `totalCommercialValue` | number |  |
| `trackingNumber` | string |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `POST /SalesShipments` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-shipment.md) for the provider-specific parameters and requirements.

