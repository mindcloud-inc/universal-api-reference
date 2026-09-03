# Stripe: List Customer Payment Methods



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customer-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customer-payment-methods?connectionId=$CONNECTION_ID&limit=25&offset=0&customer=cus_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customer": "cus_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customer-payment-methods?${params}`, {
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
| `customer` | string | yes | Example: `cus_...`. |
| `type` | string | no | Example: `card`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowRedisplay` | list | no | One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowRedisplay": "string",
      "billingDetails": {},
      "card": {},
      "created": 1,
      "customer": "string",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowRedisplay` | string |  |
| `billingDetails` | object |  |
| `card` | object |  |
| `created` | number |  |
| `customer` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET customers/:customer/payment_methods` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-payment-methods.md) for the provider-specific parameters and requirements.

