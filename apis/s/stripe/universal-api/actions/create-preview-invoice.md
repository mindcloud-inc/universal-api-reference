# Stripe: Create Preview Invoice



```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-preview-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-preview-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-preview-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | no | Example: `cus_...`. |
| `subscription` | string | no | Example: `sub_...`. |
| `schedule` | string | no | Example: `sub_sched_...`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `previewMode` | list | no | One of: `0`, `1`. |

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

Through the native Stripe API, this operation is `POST invoices/create_preview` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-preview-invoice.md) for the provider-specific parameters and requirements.

