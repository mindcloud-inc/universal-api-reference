# Stripe: List Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-subscriptions?${params}`, {
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
| `customer` | string | no | Only return subscriptions for this Stripe customer ID. Example: `cus_...`. |
| `status` | list<string> | no | Only return subscriptions with the selected Stripe subscription status. One of: `active`, `all`, `canceled`, `ended`, `incomplete`, `incomplete_expired`, `past_due`, `paused`, `trialing`, `unpaid`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionMethod` | list<string> | no | Only return subscriptions collected automatically or paid by sent invoice. One of: `charge_automatically`, `send_invoice`. |
| `price` | string | no | Only return subscriptions containing this recurring Stripe price ID. Example: `price_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAt": 1,
      "cancelAtPeriodEnd": true,
      "canceledAt": 1,
      "collectionMethod": "string",
      "created": 1,
      "currency": "string",
      "currentPeriodEnd": 1,
      "currentPeriodStart": 1,
      "customer": "string",
      "endedAt": 1,
      "id": "string",
      "items": {},
      "latestInvoice": "string",
      "metadata": {},
      "plan": {},
      "quantity": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAt` | number | Scheduled cancellation timestamp in seconds |
| `cancelAtPeriodEnd` | boolean | Whether the subscription is scheduled to cancel at the end of the current period |
| `canceledAt` | number | Cancellation request timestamp in seconds |
| `collectionMethod` | string | How recurring invoices are collected |
| `created` | number | Subscription creation timestamp in seconds |
| `currency` | string | Three-letter subscription currency code |
| `currentPeriodEnd` | number | Current billing period end timestamp in seconds |
| `currentPeriodStart` | number | Current billing period start timestamp in seconds |
| `customer` | string | Stripe customer ID that owns the subscription |
| `endedAt` | number | Timestamp when the subscription ended |
| `id` | string | Subscription ID |
| `items` | object | Subscription items and their recurring prices |
| `latestInvoice` | string | Most recent invoice ID |
| `metadata` | object | Custom subscription metadata |
| `plan` | object | Primary recurring plan details when present |
| `quantity` | number | Subscription quantity when present |
| `status` | string | Current subscription status |

## Native endpoint

Through the native Stripe API, this operation is `GET subscriptions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

