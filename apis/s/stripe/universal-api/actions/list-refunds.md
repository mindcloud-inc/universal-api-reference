# Stripe: List Refunds



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-refunds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-refunds?${params}`, {
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
| `charge` | string | no | Example: `ch_...`. |
| `paymentIntent` | string | no | Example: `pi_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "charge": "string",
      "created": 1,
      "currency": "string",
      "id": "string",
      "paymentIntent": "string",
      "reason": "string",
      "receiptNumber": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `charge` | string |  |
| `created` | number |  |
| `currency` | string |  |
| `id` | string |  |
| `paymentIntent` | string |  |
| `reason` | string |  |
| `receiptNumber` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET refunds` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-refunds.md) for the provider-specific parameters and requirements.

