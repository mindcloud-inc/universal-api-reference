# Ticket Tailor: List Discounts

Retrieves discounts from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-discounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-discounts?${params}`, {
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
      "bookingFeePercent": 1,
      "code": "string",
      "expires": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "id": "string",
      "maxRedemptions": 1,
      "name": "Ava Chen",
      "object": "string",
      "price": 1,
      "pricePercent": 1,
      "products": [
        "string"
      ],
      "ticketTypes": [
        "string"
      ],
      "timesRedeemed": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingFee` | number | Booking fee amount in cents. Could be null. |
| `bookingFeePercent` | number | Percent of the booking fee. Could be null. |
| `code` | string | Discount code |
| `expires` | object | Discount code's expiry date |
| `expires.date` | string | ISO-8601 date for the start of the event |
| `expires.formatted` | string | A formatted date string for the start of the event |
| `expires.iso` | string | ISO-8601 date and time for the start of the event |
| `expires.time` | string | Time for the start of the event |
| `expires.timezone` | string | Timezone offset for the start of the event |
| `expires.unix` | number | Unix timestamp for the start of the event |
| `id` | string | A unique identifier for the discount |
| `maxRedemptions` | number | The maximum number of times this discount can be used. |
| `name` | string | A descriptive name given to the discount |
| `object` | string |  |
| `price` | number | Price in cents. Could be null. |
| `pricePercent` | number | Percent of the price. Could be null. |
| `products` | array<string> | An array of associated products. |
| `ticketTypes` | array<string> | An array of associated ticket types. |
| `timesRedeemed` | number | The number of times that the discount was used |
| `type` | string | Type of discount. Either a fixed amount or a percentage |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/discounts` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-discounts.md) for the provider-specific parameters and requirements.

