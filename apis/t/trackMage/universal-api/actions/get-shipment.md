# TrackMage: Get Shipment

Retrieves a shipment from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment?${params}`, {
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
| `id` | string | yes | Resource identifier |

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

Through the native TrackMage API, this operation is `GET /shipments/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

