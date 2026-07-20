# TrackMage: Create Shipment

Creates a new shipment in TrackMage.

```
POST https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace` | string | yes | The workspace reference to which the shipment belongs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingNumber` | string | no | A tracking number, provided by the shipping company. |
| `orderNumbers[]` | array<string> | no | List of order numbers to which the shipment belongs. |
| `email` | string | no | Customer email address. |
| `phoneNumber` | string | no | Customer phone number. |
| `originCarrier` | string | no | The code of origin [carrier](https://trackmage.com/carriers/). Origin Carrier will be identified automatically based on Tracking Number. Sometimes the carrier cannot be identified. In that case, the system will return the error with the suggested carriers list in the payload. The value of this field can be specified only once in POST request. |
| `orders[]` | array<string> | no | List of order references to which the shipment belongs. |
| `shipmentItems[]` | array<object> | no | List of shipment items references that belong to the shipment. |
| `externalSourceIntegration` | string | no | The workflow reference to integration for ecommerce store. |
| `externalSourceSyncId` | string | no | The id of the shipment in ecommerce store (WooCommerce, Shopify, etc.). |
| `fulfillmentIntegration` | string | no | The workflow reference to integration for fulfillment source. |
| `fulfillmentSyncId` | string | no | The id of the shipment in the fulfillment source system (AliExpress, Amazon, etc.). |
| `address.addressLine1` | string | no | The street address. This field is optional. |
| `address.addressLine2` | string | no | An optional additional field for the street address. This field is optional. |
| `address.city` | string | no | The city, town, or village. This field is optional. |
| `address.company` | string | no | The company of the person associated with the address. This field is optional. |
| `address.country` | string | no | The name of the country. This field is optional. |
| `address.countryIso2` | string | no | The two-letter country code. This field is optional. |
| `address.firstName` | string | no | The first name of the person associated with the address. This field is optional. |
| `address.lastName` | string | no | The last name of the person associated with the address. This field is optional. |
| `address.postcode` | string | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `address.state` | string | no | The name of the region (province, state, prefecture, …). This field is optional. |
| `shipmentStatus.code` | string | no | A unique status code. This field is required. |
| `shipmentStatus.title` | string | no | A status name. This field is optional. |
| `shipmentStatus.description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postcode": "string",
        "state": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "daysInIdle": 1,
      "daysInTransit": 1,
      "daysSinceLastCheckpoint": 1,
      "destinationCarrier": "string",
      "destinationCountry": "string",
      "destinationCountryIso2": "string",
      "email": "ava@example.com",
      "expectedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "externalSourceIntegration": "string",
      "externalSourceIntegrationType": "string",
      "externalSourceSyncId": "string",
      "fulfillmentIntegration": "string",
      "fulfillmentSyncId": "string",
      "id": "string",
      "lastStatusUpdate": "2026-05-07T12:00:00.000Z",
      "orderNumbers": [
        "string"
      ],
      "orders": [
        "string"
      ],
      "originCarrier": "string",
      "originCountry": "string",
      "originCountryIso2": "string",
      "phoneNumber": "string",
      "review": "string",
      "reviewTotalScore": 1,
      "shipmentItems": [
        "string"
      ],
      "shipmentStatus": {
        "code": "string",
        "description": "string",
        "id": "string",
        "title": "string"
      },
      "shippedAt": "2026-05-07T12:00:00.000Z",
      "trackingNumber": "string",
      "trackingStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.addressLine1` | string |  |
| `address.addressLine2` | string |  |
| `address.city` | string |  |
| `address.company` | string |  |
| `address.country` | string |  |
| `address.countryIso2` | string |  |
| `address.firstName` | string |  |
| `address.lastName` | string |  |
| `address.postcode` | string |  |
| `address.state` | string |  |
| `createdAt` | date |  |
| `daysInIdle` | number |  |
| `daysInTransit` | number |  |
| `daysSinceLastCheckpoint` | number |  |
| `destinationCarrier` | string |  |
| `destinationCountry` | string |  |
| `destinationCountryIso2` | string |  |
| `email` | string |  |
| `expectedDeliveryDate` | date |  |
| `externalSourceIntegration` | string |  |
| `externalSourceIntegrationType` | string |  |
| `externalSourceSyncId` | string |  |
| `fulfillmentIntegration` | string |  |
| `fulfillmentSyncId` | string |  |
| `id` | string |  |
| `lastStatusUpdate` | date |  |
| `orderNumbers` | array<string> |  |
| `orders` | array<string> |  |
| `originCarrier` | string |  |
| `originCountry` | string |  |
| `originCountryIso2` | string |  |
| `phoneNumber` | string |  |
| `review` | string |  |
| `reviewTotalScore` | number |  |
| `shipmentItems` | array<string> |  |
| `shipmentStatus` | object |  |
| `shipmentStatus.code` | string |  |
| `shipmentStatus.description` | string |  |
| `shipmentStatus.id` | string |  |
| `shipmentStatus.title` | string |  |
| `shippedAt` | date |  |
| `trackingNumber` | string |  |
| `trackingStatus` | string |  |
| `updatedAt` | date |  |
| `workspace` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `POST /shipments` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

