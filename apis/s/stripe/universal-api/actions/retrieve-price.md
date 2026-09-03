# Stripe: Retrieve Price



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-price?connectionId=$CONNECTION_ID&price=price_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "price": "price_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-price?${params}`, {
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
| `price` | string | yes | Example: `price_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billingScheme": "string",
      "created": 1,
      "currency": "string",
      "id": "string",
      "lookupKey": "string",
      "nickname": "Ava Chen",
      "product": "string",
      "recurring": {},
      "type": "string",
      "unitAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billingScheme` | string |  |
| `created` | number |  |
| `currency` | string |  |
| `id` | string |  |
| `lookupKey` | string |  |
| `nickname` | string |  |
| `product` | string |  |
| `recurring` | object |  |
| `type` | string |  |
| `unitAmount` | number |  |

## Native endpoint

Through the native Stripe API, this operation is `GET prices/:price` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-price.md) for the provider-specific parameters and requirements.

