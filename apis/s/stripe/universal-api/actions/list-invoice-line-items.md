# Stripe: List Invoice Line Items



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoice-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoice-line-items?connectionId=$CONNECTION_ID&limit=25&offset=0&invoice=in_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "invoice": "in_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoice-line-items?${params}`, {
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
| `invoice` | string | yes | Example: `in_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "description": "string",
      "id": "string",
      "parent": {},
      "period": {},
      "price": {},
      "pricing": {},
      "proration": true,
      "quantity": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | string |  |
| `parent` | object |  |
| `period` | object |  |
| `price` | object |  |
| `pricing` | object |  |
| `proration` | boolean |  |
| `quantity` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET invoices/:invoice/lines` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoice-line-items.md) for the provider-specific parameters and requirements.

