# Sharetribe: Query Transactions

Retrieves transactions from Sharetribe.

```
GET https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/query-transactions?${params}`, {
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
| `createdAtStart` | date | no | Filter transactions created on or after this ISO 8601 timestamp. |
| `createdAtEnd` | date | no | Filter transactions created before this ISO 8601 timestamp. |
| `userId` | string | no | Return transactions where this user is either the customer or provider. |
| `customerId` | string | no | Return only transactions where this user is the customer. |
| `providerId` | string | no | Return only transactions where this user is the provider. |
| `listingId` | string | no | Return only transactions for this listing. |
| `lastTransitions` | string | no | Comma-separated list of last transition names to match. Accepts multiple values in one string, delimited by `,`. |
| `processNames` | string | no | Comma-separated list of transaction process names to match. Accepts multiple values in one string, delimited by `,`. |
| `states` | string | no | Comma-separated list of transaction states to match. Accepts multiple values in one string, delimited by `,`. |
| `hasBooking` | boolean | no | Filter by whether a booking is present. |
| `hasStockReservation` | boolean | no | Filter by whether a stock reservation is present. |
| `hasPayin` | boolean | no | Filter by whether the transaction has at least one pay-in. |
| `hasMessage` | boolean | no | Filter by whether the transaction has at least one message. |
| `bookingStates` | string | no | Comma-separated list of booking states to match. Accepts multiple values in one string, delimited by `,`. |
| `stockReservationStates` | string | no | Comma-separated list of stock reservation states to match. Accepts multiple values in one string, delimited by `,`. |
| `bookingStart` | string | no | Booking start range using START,END, START,, or ,END with ISO 8601 timestamps. |
| `bookingEnd` | string | no | Booking end range using START,END, START,, or ,END with ISO 8601 timestamps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `GET transactions/query` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-transactions.md) for the provider-specific parameters and requirements.

