# Stripe: List Invoices

Retrieves invoices from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amountDue": 1,
      "amountPaid": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "hostedInvoiceUrl": "https://example.com",
      "id": "string",
      "object": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number | Amount due |
| `amountPaid` | number | Amount paid |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Invoice currency |
| `customer` | string | Customer ID |
| `hostedInvoiceUrl` | string | Hosted invoice URL |
| `id` | string | Invoice ID |
| `object` | string | Stripe object type |
| `status` | string | Invoice status |
| `total` | number | Invoice total |

## Native endpoint

Through the native Stripe API, this operation is `GET invoices` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

