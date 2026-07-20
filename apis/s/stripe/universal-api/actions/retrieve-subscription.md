# Stripe: Retrieve Subscription

Retrieves a subscription from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription?connectionId=$CONNECTION_ID&subscriptionExposedId=sub_1MowQVLkdIwHu7ixeRlqHVzs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionExposedId": "sub_1MowQVLkdIwHu7ixeRlqHVzs"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription?${params}`, {
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
| `subscriptionExposedId` | string | yes | Subscription identifier. Example: `sub_1MowQVLkdIwHu7ixeRlqHVzs`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native Stripe API, this operation is `GET subscriptions/:subscription_exposed_id` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription.md) for the provider-specific parameters and requirements.

