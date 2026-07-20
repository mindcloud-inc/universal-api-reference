# TicketSource: Get Seat

Retrieves a seat from the TicketSource account.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-seat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-seat?connectionId=$CONNECTION_ID&seatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-seat?${params}`, {
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
| `seatId` | string | yes | The unique identifier for a Seat record |

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

Through the native TicketSource API, this operation is `GET /seats/{SeatId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-seat.md) for the provider-specific parameters and requirements.

