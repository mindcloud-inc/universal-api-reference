# Flexport: List Bookings

Retrieves bookings from your Flexport account.

```
GET https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-bookings?${params}`, {
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
      "airBooking": {},
      "bookingLineItems": {},
      "cargo": {},
      "cargoReadyDate": "2026-05-07T12:00:00.000Z",
      "consigneeEntity": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "destinationAddress": {},
      "flexId": "string",
      "id": 1,
      "metadata": {},
      "name": "Ava Chen",
      "notifyParty": {},
      "oceanBooking": {},
      "originAddress": {},
      "quoteStatus": "string",
      "shipment": {},
      "shipperEntity": {},
      "specialInstructions": "string",
      "status": "string",
      "transportationMode": "string",
      "truckingBooking": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com",
      "wantsBco": true,
      "wantsExportCustomsService": true,
      "wantsFlexportFreight": true,
      "wantsImportCustomsService": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airBooking` | object |  |
| `bookingLineItems` | object |  |
| `cargo` | object |  |
| `cargoReadyDate` | date |  |
| `consigneeEntity` | object |  |
| `createdAt` | date |  |
| `deliveryDate` | date |  |
| `destinationAddress` | object |  |
| `flexId` | string |  |
| `id` | number |  |
| `metadata` | object |  |
| `name` | string |  |
| `notifyParty` | object |  |
| `oceanBooking` | object |  |
| `originAddress` | object |  |
| `quoteStatus` | string |  |
| `shipment` | object |  |
| `shipperEntity` | object |  |
| `specialInstructions` | string |  |
| `status` | string |  |
| `transportationMode` | string |  |
| `truckingBooking` | object |  |
| `updatedAt` | date |  |
| `userEmail` | string |  |
| `wantsBco` | boolean |  |
| `wantsExportCustomsService` | boolean |  |
| `wantsFlexportFreight` | boolean |  |
| `wantsImportCustomsService` | boolean |  |

## Native endpoint

Through the native Flexport API, this operation is `GET /bookings` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

