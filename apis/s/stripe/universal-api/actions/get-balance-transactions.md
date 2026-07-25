# Stripe: Get Balance Transactions



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-balance-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-balance-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
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
| `stripeApiKey` | string | no |  |
| `payoutId` | string | no |  |
| `limit` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stripe API returns.

## Native endpoint

Through the native Stripe API, this operation is `GET /balance_transactions?payout={{payoutId}}&limit={{limit}}&expand[]=data.source&expand[]=data.source.charge` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance-transactions.md) for the provider-specific parameters and requirements.

