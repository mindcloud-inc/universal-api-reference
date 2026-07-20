# Easyship: Create Shipment

Creates a new shipment in Easyship.

```
POST https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parcels[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parcels[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `originAddressId` | string | no | Existing Easyship origin address ID. Leave blank if you provide the origin address object instead. |
| `originAddress` | object | no | Origin address object. |
| `originAddress.line1` | string | no | Origin address line 1. |
| `originAddress.line2` | string | no | Origin address line 2. |
| `originAddress.city` | string | no | Origin city. |
| `originAddress.state` | string | no | Origin state or province. |
| `originAddress.postalCode` | string | no | Origin postal code. |
| `originAddress.countryAlpha2` | string | no | Origin country code. |
| `originAddress.companyName` | string | no | Origin company name. |
| `originAddress.contactName` | string | no | Origin contact name. |
| `originAddress.contactEmail` | string | no | Origin contact email. |
| `originAddress.contactPhone` | string | no | Origin contact phone. |
| `destinationAddress` | object | no | Destination address object. |
| `destinationAddress.line1` | string | no | Destination address line 1. |
| `destinationAddress.line2` | string | no | Destination address line 2. |
| `destinationAddress.city` | string | no | Destination city. |
| `destinationAddress.state` | string | no | Destination state or province. |
| `destinationAddress.postalCode` | string | no | Destination postal code. |
| `destinationAddress.countryAlpha2` | string | no | Destination country code. |
| `destinationAddress.companyName` | string | no | Destination company name. |
| `destinationAddress.contactName` | string | no | Destination contact name. |
| `destinationAddress.contactEmail` | string | no | Destination contact email. |
| `destinationAddress.contactPhone` | string | no | Destination contact phone. |
| `parcels[]` | array<object> | yes | Shipment parcels array. |
| `parcels[].items[]` | array<object> | no | Items included in a parcel. |
| `parcels[].box` | object | no | Parcel box details. |
| `parcels[].totalActualWeight` | number | no | Total parcel weight in kilograms. |
| `parcels[].box.slug` | string | no | Courier or custom box slug. |
| `parcels[].box.length` | number | no | Parcel box length. |
| `parcels[].box.width` | number | no | Parcel box width. |
| `parcels[].box.height` | number | no | Parcel box height. |
| `parcels[].items[].description` | string | no | Description of the parcel item. |
| `parcels[].items[].category` | string | no | Item category name or slug. |
| `parcels[].items[].sku` | string | no | Parcel item SKU. |
| `parcels[].items[].hsCode` | string | no | Parcel item HS code. |
| `parcels[].items[].containsBatteryPi966` | boolean | no | Whether the item applies PI966. |
| `parcels[].items[].containsBatteryPi967` | boolean | no | Whether the item applies PI967. |
| `parcels[].items[].containsLiquids` | boolean | no | Whether the item contains liquids. |
| `parcels[].items[].originCountryAlpha2` | string | no | Item origin country. |
| `parcels[].items[].quantity` | number | no | Parcel item quantity. |
| `parcels[].items[].dimensions` | object | no | Parcel item dimensions object. |
| `parcels[].items[].dimensions.length` | number | no | Parcel item length. |
| `parcels[].items[].dimensions.width` | number | no | Parcel item width. |
| `parcels[].items[].dimensions.height` | number | no | Parcel item height. |
| `parcels[].items[].actualWeight` | number | no | Parcel item actual weight. |
| `parcels[].items[].declaredCurrency` | string | no | Parcel item declared currency. |
| `parcels[].items[].declaredCustomsValue` | number | no | Parcel item declared customs value. |
| `parcels[].items[].product` | object | no | Parcel product reference object. |
| `parcels[].items[].product.id` | string | no | Product ID for product-backed parcel items. |
| `parcels[].items[].product.sku` | string | no | Product SKU for product-backed parcel items. |
| `parcels[].items[].id` | string | no | Item ID for return shipments. |

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

Through the native Easyship API, this operation is `POST /shipments` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

