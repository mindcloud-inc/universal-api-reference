# Stripe: Retrieve Customer

Retrieves a customer from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&customer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-customer?${params}`, {
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
| `customer` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "currency": "string",
      "delinquent": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Default currency |
| `delinquent` | boolean | Whether the customer is delinquent |
| `email` | string | Customer email |
| `id` | string | Customer ID |
| `name` | string | Customer name |
| `object` | string | Stripe object type |

## Native endpoint

Through the native Stripe API, this operation is `GET customers/:customer` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

