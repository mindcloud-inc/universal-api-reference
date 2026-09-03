# Stripe: List Credit Notes



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-credit-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-credit-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-credit-notes?${params}`, {
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
| `invoice` | string | no | Example: `in_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "id": "string",
      "invoice": "string",
      "lines": {},
      "number": "string",
      "pdf": "string",
      "reason": "string",
      "status": "string",
      "total": 1,
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
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `id` | string |  |
| `invoice` | string |  |
| `lines` | object |  |
| `number` | string |  |
| `pdf` | string |  |
| `reason` | string |  |
| `status` | string |  |
| `total` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET credit_notes` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credit-notes.md) for the provider-specific parameters and requirements.

