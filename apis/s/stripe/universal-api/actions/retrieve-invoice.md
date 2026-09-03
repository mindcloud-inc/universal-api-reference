# Stripe: Retrieve Invoice



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-invoice?connectionId=$CONNECTION_ID&invoice=in_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice": "in_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-invoice?${params}`, {
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
      "amountDue": 1,
      "amountPaid": 1,
      "amountRemaining": 1,
      "billingReason": "string",
      "collectionMethod": "string",
      "created": 1,
      "currency": "string",
      "customer": "string",
      "dueDate": 1,
      "hostedInvoiceUrl": "https://example.com",
      "id": "string",
      "invoicePdf": "string",
      "lines": {},
      "status": "string",
      "subscription": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number |  |
| `amountPaid` | number |  |
| `amountRemaining` | number |  |
| `billingReason` | string |  |
| `collectionMethod` | string |  |
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `dueDate` | number |  |
| `hostedInvoiceUrl` | string |  |
| `id` | string |  |
| `invoicePdf` | string |  |
| `lines` | object |  |
| `status` | string |  |
| `subscription` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Stripe API, this operation is `GET invoices/:invoice` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-invoice.md) for the provider-specific parameters and requirements.

