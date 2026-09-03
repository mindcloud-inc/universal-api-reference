# Stripe: List Checkout Sessions



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-sessions?${params}`, {
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
| `customer` | string | no | Example: `cus_...`. |
| `status` | list | no | One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentIntent` | string | no | Example: `pi_...`. |
| `subscription` | string | no | Example: `sub_...`. |
| `paymentLink` | string | no | Example: `plink_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountTotal": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "customerDetails": {},
      "expiresAt": 1,
      "id": "string",
      "invoice": "string",
      "metadata": {},
      "mode": "string",
      "paymentIntent": "string",
      "paymentStatus": "string",
      "status": "string",
      "subscription": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountTotal` | number |  |
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `customerDetails` | object |  |
| `expiresAt` | number |  |
| `id` | string |  |
| `invoice` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `paymentIntent` | string |  |
| `paymentStatus` | string |  |
| `status` | string |  |
| `subscription` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET checkout/sessions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkout-sessions.md) for the provider-specific parameters and requirements.

