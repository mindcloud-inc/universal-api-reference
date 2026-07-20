# Easyship: Get Shipment

Retrieves a shipment from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipment?connectionId=$CONNECTION_ID&shipmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipment?${params}`, {
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
| `shipmentId` | string | yes | The Easyship shipment ID. |

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
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string"
      },
      "easyshipShipmentId": "string",
      "incoterms": "string",
      "insurance": {
        "insuredAmount": 1,
        "insuredCurrency": "string",
        "isInsured": true
      },
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
      "rates": [
        [
          {}
        ]
      ],
      "setAsResidential": true,
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
| `destinationAddress.line1` | string |  |
| `destinationAddress.line2` | string |  |
| `destinationAddress.postalCode` | string |  |
| `destinationAddress.state` | string |  |
| `easyshipShipmentId` | string |  |
| `incoterms` | string |  |
| `insurance` | object |  |
| `insurance.insuredAmount` | number |  |
| `insurance.insuredCurrency` | string |  |
| `insurance.isInsured` | boolean |  |
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
| `parcels[].box` | object |  |
| `parcels[].box.outerDimensions` | object |  |
| `parcels[].box.outerDimensions.height` | number |  |
| `parcels[].box.outerDimensions.length` | number |  |
| `parcels[].box.outerDimensions.width` | number |  |
| `parcels[].box.slug` | string |  |
| `parcels[].box.type` | string |  |
| `parcels[].box.weight` | number |  |
| `parcels[].id` | string |  |
| `parcels[].items[]` | array<object> |  |
| `parcels[].items[].actualWeight` | number |  |
| `parcels[].items[].declaredCurrency` | string |  |
| `parcels[].items[].declaredCustomsValue` | number |  |
| `parcels[].items[].description` | string |  |
| `parcels[].items[].dimensions` | object |  |
| `parcels[].items[].dimensions.height` | number |  |
| `parcels[].items[].dimensions.length` | number |  |
| `parcels[].items[].dimensions.width` | number |  |
| `parcels[].items[].hsCode` | string |  |
| `parcels[].items[].id` | string |  |
| `parcels[].items[].originCountryAlpha2` | string |  |
| `parcels[].items[].quantity` | number |  |
| `parcels[].items[].sku` | string |  |
| `parcels[].totalActualWeight` | number |  |
| `pickupState` | string |  |
| `rates[]` | array<object> |  |
| `rates[].courierService` | object |  |
| `rates[].courierService.id` | string |  |
| `rates[].courierService.name` | string |  |
| `rates[].courierService.umbrellaName` | string |  |
| `rates[].currency` | string |  |
| `rates[].incoterms` | string |  |
| `rates[].maxDeliveryTime` | number |  |
| `rates[].minDeliveryTime` | number |  |
| `rates[].shipmentCharge` | number |  |
| `rates[].shipmentChargeTotal` | number |  |
| `rates[].totalCharge` | number |  |
| `rates[].trackingRating` | number |  |
| `setAsResidential` | boolean |  |
| `shipmentState` | string |  |
| `shippingDocuments[]` | array<object> |  |
| `trackingPageUrl` | string |  |
| `trackings[]` | array<object> |  |
| `updatedAt` | string |  |
| `warehouseState` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /shipments/:shipment_id` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

