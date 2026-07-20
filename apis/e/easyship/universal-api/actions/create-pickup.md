# Easyship: Create Pickup

Creates a new pickup in Easyship.

```
POST https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-pickup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-pickup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courierServiceId": "string",
  "selectedDate": "string",
  "easyshipShipmentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-pickup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courierServiceId": "string",
    "selectedDate": "string",
    "easyshipShipmentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courierServiceId` | string | yes | The unique identifier for the courier service. |
| `timeSlotId` | string | no | Pickup time slot ID. |
| `selectedDate` | string | yes | Selected date for pickup. |
| `selectedFromTime` | string | no | Selected pickup start time. |
| `selectedToTime` | string | no | Selected pickup end time. |
| `easyshipShipmentIds[]` | array<string> | yes | Shipment IDs to include in the pickup request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "companyName": "Ava Chen",
        "contactEmail": "ava@example.com",
        "countryAlpha2": "string",
        "id": "string",
        "line1": "string",
        "postalCode": "string",
        "status": "string"
      },
      "courierService": {
        "id": "string",
        "name": "Ava Chen",
        "umbrellaName": "Ava Chen"
      },
      "easyshipPickupId": "string",
      "pickupFee": 1,
      "pickupReferenceNumber": "string",
      "pickupState": "string",
      "providerName": "Ava Chen",
      "selectedFromTime": "2026-05-07T12:00:00.000Z",
      "selectedToTime": "2026-05-07T12:00:00.000Z",
      "shipmentsCount": 1,
      "totalActualWeight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string | Pickup city. |
| `address.companyName` | string | Pickup company name. |
| `address.contactEmail` | string | Pickup contact email. |
| `address.countryAlpha2` | string | Pickup country code. |
| `address.id` | string | Pickup address ID. |
| `address.line1` | string | Pickup address line 1. |
| `address.postalCode` | string | Pickup postal code. |
| `address.status` | string | Pickup address status. |
| `courierService.id` | string | Courier service ID. |
| `courierService.name` | string | Courier service name. |
| `courierService.umbrellaName` | string | Courier umbrella name. |
| `easyshipPickupId` | string | The Easyship pickup ID. |
| `pickupFee` | number | Pickup fee amount. |
| `pickupReferenceNumber` | string | Pickup reference number when available. |
| `pickupState` | string | Current pickup state. |
| `providerName` | string | Pickup provider name. |
| `selectedFromTime` | date | Pickup start time. |
| `selectedToTime` | date | Pickup end time. |
| `shipmentsCount` | number | Number of shipments in the pickup. |
| `totalActualWeight` | number | Total shipment weight in the pickup. |

## Native endpoint

Through the native Easyship API, this operation is `POST /pickups` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pickup.md) for the provider-specific parameters and requirements.

