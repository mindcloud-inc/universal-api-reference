# Easyship: List Shipments

Retrieves a list of shipments from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "courierService": {
        "courierId": "string",
        "easyshipCourierService": true,
        "id": "string",
        "name": "Ava Chen",
        "umbrellaName": "Ava Chen"
      },
      "createdAt": "string",
      "currency": "string",
      "deliveryState": "string",
      "destinationAddress": {
        "city": "string",
        "companyName": "Ava Chen",
        "contactEmail": "ava@example.com",
        "contactName": "Ava Chen",
        "contactPhone": "string",
        "countryAlpha2": "string",
        "deliveryInstructions": "string",
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string"
      },
      "easyshipShipmentId": "string",
      "labelGeneratedAt": "string",
      "labelPaidAt": "string",
      "labelState": "string",
      "originAddress": {
        "city": "string",
        "companyName": "Ava Chen",
        "contactEmail": "ava@example.com",
        "contactName": "Ava Chen",
        "contactPhone": "string",
        "countryAlpha2": "string",
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string"
      },
      "parcels": [
        [
          {}
        ]
      ],
      "pickupState": "string",
      "shipmentState": "string",
      "shippingDocuments": [
        [
          {}
        ]
      ],
      "trackingPageUrl": "https://example.com",
      "trackings": [
        [
          {}
        ]
      ],
      "updatedAt": "string",
      "warehouseState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courierService` | object |  |
| `courierService.courierId` | string |  |
| `courierService.easyshipCourierService` | boolean |  |
| `courierService.id` | string |  |
| `courierService.name` | string |  |
| `courierService.umbrellaName` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `deliveryState` | string |  |
| `destinationAddress` | object |  |
| `destinationAddress.city` | string |  |
| `destinationAddress.companyName` | string |  |
| `destinationAddress.contactEmail` | string |  |
| `destinationAddress.contactName` | string |  |
| `destinationAddress.contactPhone` | string |  |
| `destinationAddress.countryAlpha2` | string |  |
| `destinationAddress.deliveryInstructions` | string |  |
| `destinationAddress.line1` | string |  |
| `destinationAddress.line2` | string |  |
| `destinationAddress.postalCode` | string |  |
| `destinationAddress.state` | string |  |
| `easyshipShipmentId` | string |  |
| `labelGeneratedAt` | string |  |
| `labelPaidAt` | string |  |
| `labelState` | string |  |
| `originAddress` | object |  |
| `originAddress.city` | string |  |
| `originAddress.companyName` | string |  |
| `originAddress.contactEmail` | string |  |
| `originAddress.contactName` | string |  |
| `originAddress.contactPhone` | string |  |
| `originAddress.countryAlpha2` | string |  |
| `originAddress.line1` | string |  |
| `originAddress.line2` | string |  |
| `originAddress.postalCode` | string |  |
| `originAddress.state` | string |  |
| `parcels[]` | array<object> |  |
| `parcels[].id` | string |  |
| `parcels[].items[]` | array<object> |  |
| `parcels[].items[].category` | string |  |
| `parcels[].items[].declaredCurrency` | string |  |
| `parcels[].items[].declaredCustomsValue` | number |  |
| `parcels[].items[].description` | string |  |
| `parcels[].items[].id` | string |  |
| `parcels[].items[].quantity` | number |  |
| `parcels[].items[].sku` | string |  |
| `parcels[].totalActualWeight` | number |  |
| `pickupState` | string |  |
| `shipmentState` | string |  |
| `shippingDocuments[]` | array<object> |  |
| `shippingDocuments[].category` | string |  |
| `shippingDocuments[].format` | string |  |
| `shippingDocuments[].pageSize` | string |  |
| `shippingDocuments[].required` | boolean |  |
| `shippingDocuments[].url` | string |  |
| `trackingPageUrl` | string |  |
| `trackings[]` | array<object> |  |
| `trackings[].handler` | string |  |
| `trackings[].legNumber` | number |  |
| `trackings[].trackingNumber` | string |  |
| `trackings[].trackingState` | string |  |
| `updatedAt` | string |  |
| `warehouseState` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /shipments` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

