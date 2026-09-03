# Stripe: Retrieve Charge



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-charge?connectionId=$CONNECTION_ID&charge=ch_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "charge": "ch_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-charge?${params}`, {
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
| `charge` | string | yes | Example: `ch_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountCaptured": 1,
      "amountRefunded": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "description": "string",
      "disputed": true,
      "id": "string",
      "outcome": {},
      "paid": true,
      "paymentIntent": "string",
      "paymentMethod": "string",
      "receiptUrl": "https://example.com",
      "refunded": true,
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
| `amountCaptured` | number |  |
| `amountRefunded` | number |  |
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `description` | string |  |
| `disputed` | boolean |  |
| `id` | string |  |
| `outcome` | object |  |
| `paid` | boolean |  |
| `paymentIntent` | string |  |
| `paymentMethod` | string |  |
| `receiptUrl` | string |  |
| `refunded` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET charges/:charge` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-charge.md) for the provider-specific parameters and requirements.

