# Stripe: Retrieve Credit Note



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-credit-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-credit-note?connectionId=$CONNECTION_ID&creditNote=cn_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "creditNote": "cn_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-credit-note?${params}`, {
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
| `creditNote` | string | yes | Example: `cn_...`. |

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

Through the native Stripe API, this operation is `GET credit_notes/:creditNote` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-credit-note.md) for the provider-specific parameters and requirements.

