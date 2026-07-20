# TicketSource: List Booking Seats

Retrieves seats for a booking from TicketSource.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-booking-seats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-booking-seats?connectionId=$CONNECTION_ID&limit=25&offset=0&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bookingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-booking-seats?${params}`, {
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
| `bookingId` | string | yes | The unique identifier for a Booking record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "attendee": {
          "company": {
            "name": "Ava Chen",
            "title": "string"
          },
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "telephone": "string",
          "title": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "isBooked": true,
        "isCancelled": true,
        "priceCategory": "string",
        "reference": {
          "row": "string",
          "seat": "string"
        },
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "booking": "https://example.com",
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.attendee.company.name` | string |  |
| `attributes.attendee.company.title` | string |  |
| `attributes.attendee.email` | string |  |
| `attributes.attendee.firstName` | string |  |
| `attributes.attendee.lastName` | string |  |
| `attributes.attendee.telephone` | string |  |
| `attributes.attendee.title` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.isBooked` | boolean |  |
| `attributes.isCancelled` | boolean |  |
| `attributes.priceCategory` | string |  |
| `attributes.reference.row` | string |  |
| `attributes.reference.seat` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.booking` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /bookings/{BookingId}/seats` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-booking-seats.md) for the provider-specific parameters and requirements.

