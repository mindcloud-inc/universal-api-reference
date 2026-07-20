# Ticket Tailor: List Products

Retrieves products from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-products?${params}`, {
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
      "bookingFee": 1,
      "createdAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "currency": "string",
      "description": "string",
      "eventSeriesIds": [
        "string"
      ],
      "id": "string",
      "image": "string",
      "instructions": "string",
      "issuedCount": 1,
      "issueTicketVoucher": "string",
      "linkedToAllEventSeries": "https://example.com",
      "membershipTypeId": "string",
      "name": "Ava Chen",
      "object": "string",
      "price": 1,
      "quantity": 1,
      "quantityPerEventOccurrence": 1,
      "sellInStore": "string",
      "status": "string",
      "updatedAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "voucherId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingFee` | number | Optional booking fee in cents which is charged per product to the customer and the funds are paid to you. We would recommend charging no more than 10% of the product price. |
| `createdAt` | object | Date and time when the product was created |
| `createdAt.date` | string | ISO-8601 date for the created at date |
| `createdAt.formatted` | string | A formatted date string for the create at date |
| `createdAt.iso` | string | ISO-8601 date and time for the created at date |
| `createdAt.time` | string | Time of the end of the created at date |
| `createdAt.timezone` | string | Timezone offset for the created at date |
| `createdAt.unix` | number | Unix timestamp for for the created at date |
| `currency` | string | Information about the currency the product is configured to use |
| `description` | string | Description of the product |
| `eventSeriesIds` | array<string> | List of associated event series IDs |
| `id` | string |  |
| `image` | string | Image associated with the product |
| `instructions` | string | Instructions on how to use the product |
| `issuedCount` | number | Number of sold products |
| `issueTicketVoucher` | string | A boolean value indicating whether a QR code is to be issued for the product |
| `linkedToAllEventSeries` | string | A 'true' or 'false' value to determine if the product is linked to all the event series |
| `membershipTypeId` | string | The ID of the membership type associated with the product |
| `name` | string | Name of the product |
| `object` | string |  |
| `price` | number | Price in cents. Could be null. |
| `quantity` | number | Number available for purchase for all event occurrences |
| `quantityPerEventOccurrence` | number | Number available for purchase per event occurrence |
| `sellInStore` | string | A boolean value indicating whether product is being sold in store |
| `status` | string | Status of the product |
| `updatedAt` | object |  |
| `updatedAt.date` | string | ISO-8601 date for the updated timestamp of the product |
| `updatedAt.formatted` | string | A formatted date string for the updated timestamp of the product |
| `updatedAt.iso` | string | ISO-8601 date and time for the updated timestamp of the product |
| `updatedAt.time` | string | Time of the updated timestamp of the product |
| `updatedAt.timezone` | string | Timezone offset for the updated timestamp of the product |
| `updatedAt.unix` | number | Unix timestamp for when the product was updated |
| `voucherId` | string | The ID of the voucher of type gift card associated with the product |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/products` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

