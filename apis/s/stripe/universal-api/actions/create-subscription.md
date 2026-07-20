# Stripe: Create Subscription

Creates a new subscription in Stripe.

```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "cus_NffrFeUfNV2Hib"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "cus_NffrFeUfNV2Hib"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | Identifier of the customer to subscribe. Example: `cus_NffrFeUfNV2Hib`. |
| `item0Price` | string | no | Price ID for each subscription item. Example: `price_1MtGUsLkdIwHu7ix1be5Ljaj`. |
| `item0Quantity` | number | no | Quantity for each subscription item. Example: `1`. |
| `defaultPaymentMethod` | string | no | Payment method attached to invoices for this subscription. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentBehavior` | list<string> | no | How Stripe handles the first invoice payment. One of: `allow_incomplete`, `default_incomplete`, `error_if_incomplete`. |
| `collectionMethod` | list<string> | no | How to collect payment for this subscription. One of: `charge_automatically`, `send_invoice`. |
| `trialEnd` | string | no | Trial end timestamp or now. |
| `metadata` | object | no | Metadata key-value pairs for the subscription. |
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

Through the native Stripe API, this operation is `POST subscriptions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

