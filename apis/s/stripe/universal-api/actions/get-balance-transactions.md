# Stripe: Get Balance Transactions



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-balance-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-balance-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-balance-transactions?${params}`, {
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
| `payoutId` | string | no | Only transactions included in this automatic Stripe payout. Leave blank to list all balance transactions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `created` | object | no | Only return records created during this date interval. |
| `created.gt` | date | no | After this date, exclusive. |
| `created.gte` | date | no | On or after this date, inclusive. |
| `created.lt` | date | no | Before this date, exclusive. |
| `created.lte` | date | no | On or before this date, inclusive. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stripe API returns.

## Native endpoint

Through the native Stripe API, this operation is `GET /balance_transactions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-balance-transactions.md) for the provider-specific parameters and requirements.

