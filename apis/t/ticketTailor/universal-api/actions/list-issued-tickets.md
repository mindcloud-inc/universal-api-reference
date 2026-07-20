# Ticket Tailor: List Issued Tickets

Retrieves issued tickets from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-issued-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-issued-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-issued-tickets?${params}`, {
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
      "addOnId": "string",
      "barcode": "string",
      "barcodeUrl": "https://example.com",
      "checkedIn": "string",
      "createdAt": 1,
      "customQuestions": [
        {
          "answer": "string",
          "question": "string"
        }
      ],
      "description": "string",
      "email": "ava@example.com",
      "eventId": "string",
      "eventSeriesId": "string",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "groupTicketBarcode": "string",
      "id": "string",
      "lastName": "Chen",
      "listedCurrency": {
        "baseMultiplier": 1,
        "code": "string"
      },
      "listedPrice": 1,
      "object": "string",
      "orderId": "string",
      "qrCodeUrl": "https://example.com",
      "reference": "string",
      "reservation": "string",
      "source": "string",
      "status": "string",
      "ticketTypeId": "string",
      "updatedAt": 1,
      "voidedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addOnId` | string | A unique identifier for the associated product |
| `barcode` | string | Barcode text value |
| `barcodeUrl` | string | URL to barcode image |
| `checkedIn` | string | Returns whether or not issued ticket is checked in |
| `createdAt` | number | Timestamp when issued ticket was created |
| `customQuestions` | array<object> | Buyer provided answers to custom questions in checkout |
| `customQuestions[].answer` | string |  |
| `customQuestions[].question` | string |  |
| `description` | string |  |
| `email` | string | The order email address |
| `eventId` | string | ID of the event issued ticket belongs to |
| `eventSeriesId` | string | ID of the event series the issued ticket belongs to |
| `firstName` | string | First name of attendee |
| `fullName` | string | Full name of attendee |
| `groupTicketBarcode` | string | Barcode for group ticket, if it is part of one |
| `id` | string | A unique identifier for the issued ticket |
| `lastName` | string | Last name of attendee |
| `listedCurrency` | object | List currency of the ticket type at the time of purchase |
| `listedCurrency.baseMultiplier` | number |  |
| `listedCurrency.code` | string |  |
| `listedPrice` | number | List price of the ticket type at the time of purchase |
| `object` | string |  |
| `orderId` | string | A unique identifier for the order |
| `qrCodeUrl` | string | URL to QR code image |
| `reference` | string | An external reference for imported tickets (via the API or Dashboard) |
| `reservation` | string | Reservation from seating chart where applicable |
| `source` | string |  |
| `status` | string |  |
| `ticketTypeId` | string | ID of the ticket type |
| `updatedAt` | number | Timestamp when issued ticket was last updated |
| `voidedAt` | number | Timestamp when issued ticket was voided |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/issued_tickets` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issued-tickets.md) for the provider-specific parameters and requirements.

