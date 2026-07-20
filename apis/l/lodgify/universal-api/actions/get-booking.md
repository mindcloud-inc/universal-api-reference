# Lodgify: Get Booking

Retrieves details for a booking from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-booking?connectionId=$CONNECTION_ID&reservationId=19199854" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reservationId": "19199854"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-booking?${params}`, {
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
| `reservationId` | number | yes | Reservation identifier from Lodgify. Example: `19199854`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountToPay": 1,
      "arrival": "2026-05-07T12:00:00.000Z",
      "bookingType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": {},
      "dateDeleted": "2026-05-07T12:00:00.000Z",
      "departure": "2026-05-07T12:00:00.000Z",
      "guest": {},
      "id": 1,
      "isDeleted": true,
      "isReplied": true,
      "people": 1,
      "propertyId": 1,
      "propertyName": "Ava Chen",
      "rooms": [
        {}
      ],
      "source": "string",
      "sourceText": "string",
      "status": "string",
      "threadUid": "string",
      "totalAmount": 1,
      "totalGuestBreakdown": {},
      "totalPaid": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "upgradedEnquiryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountToPay` | number | Remaining balance. |
| `arrival` | date | Arrival date. |
| `bookingType` | string | Booking type. |
| `createdAt` | date | Created timestamp. |
| `currency` | object | Reservation currency. |
| `dateDeleted` | date | Deletion timestamp. |
| `departure` | date | Departure date. |
| `guest` | object | Guest details. |
| `id` | number | Reservation ID. |
| `isDeleted` | boolean | Whether the reservation is deleted. |
| `isReplied` | boolean | Whether the reservation has a reply. |
| `people` | number | Guest count. |
| `propertyId` | number | Property ID. |
| `propertyName` | string | Property name. |
| `rooms` | array<object> | Booked rooms. |
| `source` | string | Reservation source. |
| `sourceText` | string | Reservation source label. |
| `status` | string | Reservation status. |
| `threadUid` | string | Reservation thread UID. |
| `totalAmount` | number | Total reservation amount. |
| `totalGuestBreakdown` | object | Guest breakdown. |
| `totalPaid` | number | Total amount paid. |
| `type` | string | Reservation type. |
| `updatedAt` | date | Updated timestamp. |
| `upgradedEnquiryId` | string | Upgraded enquiry ID. |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v1/reservation/booking/:id` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

