# Eventzilla: List Event Transactions

Retrieves transactions for an event from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-transactions?${params}`, {
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
| `eventId` | number | yes | The Eventzilla event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyerFirstName": "Ava",
      "buyerLastName": "Chen",
      "checkoutId": 1,
      "comments": "string",
      "email": "ava@example.com",
      "eventDate": "2026-05-07T12:00:00.000Z",
      "eventId": 1,
      "eventzillaFee": 1,
      "paymentType": "string",
      "promoCode": "string",
      "refno": "string",
      "ticketsInTransaction": 1,
      "title": "string",
      "transactionAmount": 1,
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionDiscount": 1,
      "transactionStatus": "string",
      "transactionTax": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerFirstName` | string |  |
| `buyerLastName` | string |  |
| `checkoutId` | number |  |
| `comments` | string |  |
| `email` | string |  |
| `eventDate` | date |  |
| `eventId` | number |  |
| `eventzillaFee` | number |  |
| `paymentType` | string |  |
| `promoCode` | string |  |
| `refno` | string |  |
| `ticketsInTransaction` | number |  |
| `title` | string |  |
| `transactionAmount` | number |  |
| `transactionDate` | date |  |
| `transactionDiscount` | number |  |
| `transactionStatus` | string |  |
| `transactionTax` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /events/:eventid/transactions` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-transactions.md) for the provider-specific parameters and requirements.

