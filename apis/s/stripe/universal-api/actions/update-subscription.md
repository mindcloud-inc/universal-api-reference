# Stripe: Update Subscription

Updates an existing subscription in Stripe.

```
PUT https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionExposedId": "sub_1MowQVLkdIwHu7ixeRlqHVzs"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionExposedId": "sub_1MowQVLkdIwHu7ixeRlqHVzs"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionExposedId` | string | yes | Subscription identifier. Example: `sub_1MowQVLkdIwHu7ixeRlqHVzs`. |
| `item0Id` | string | no | Existing subscription item ID. Example: `si_NcLYdDxLHxlFo7`. |
| `item0Price` | string | no | Replacement price for item. Example: `price_1MtGUsLkdIwHu7ix1be5Ljaj`. |
| `item0Quantity` | number | no | Updated quantity for item. |
| `defaultPaymentMethod` | string | no | Default payment method for this subscription. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cancelAtPeriodEnd` | boolean | no | Whether to cancel at current period end. Example: `false`. |
| `prorationBehavior` | list<string> | no | How prorations are handled for updates. One of: `always_invoice`, `create_prorations`, `none`. |
| `paymentBehavior` | list<string> | no | How Stripe handles payment changes. One of: `allow_incomplete`, `default_incomplete`, `error_if_incomplete`, `pending_if_incomplete`. |
| `trialEnd` | string | no | Trial end timestamp or now. |
| `metadata` | object | no | Metadata key-value pairs. |
| `expand` | list<string> | no | Fields to expand in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAt": 1,
      "cancelAtPeriodEnd": true,
      "currentPeriodEnd": 1,
      "currentPeriodStart": 1,
      "customer": "string",
      "defaultPaymentMethod": "string",
      "id": "string",
      "items": {},
      "latestInvoice": "string",
      "metadata": {},
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAt` | number |  |
| `cancelAtPeriodEnd` | boolean |  |
| `currentPeriodEnd` | number |  |
| `currentPeriodStart` | number |  |
| `customer` | string |  |
| `defaultPaymentMethod` | string |  |
| `id` | string |  |
| `items` | object |  |
| `latestInvoice` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `POST subscriptions/:subscription_exposed_id` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

